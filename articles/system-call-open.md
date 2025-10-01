---
title: "O_EXCLで学ぶ：アトミック操作とレースコンディション"
emoji: "👏"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["linux"]
published: false
---

## **1. はじめに**

* Linuxプログラミングを学んでいて出会った `open(O_CREAT | O_EXCL)`。
* 最初は「ファイルを安全に作成するための便利なフラグ」くらいに思っていた。
* しかしその背後には**プロセスの並行実行**や**アトミック操作**という奥深い意味があった。
* 本記事では、このフラグを入り口に、システムコール、アトミック、そして**タイムスライスとレースコンディション**について考えていく。

---

## **2. open(O_CREAT | O_EXCL) の役割と危険なパターン**

### **2.1 フラグの意味**

* **O_CREAT**：ファイルがなければ新規作成する
* **O_EXCL**：ファイルがすでに存在すればエラー（`EEXIST`）を返す

この組み合わせにより、「存在確認」と「新規作成」を一度に実行できる。

### **2.2 悪い例：`access()` → `open()`**

存在確認と作成を分けて書くと、間に他のプロセスが割り込む可能性がある。
これは**TOCTOU（Time Of Check To Time Of Use）問題**と呼ばれる。

```c
if (access("file.txt", F_OK) == -1) {
    open("file.txt", O_WRONLY | O_CREAT); // ← ここで割り込みが入るかも
}
```

---

## **3. レースコンディションはなぜ起きるのか**

### **3.1 タイムスライスとは**

* OSは複数プロセスを同時に動いているように見せるため、CPU時間を細かく分割して使わせる。
* 1つのプロセスがCPUを占有できる最大時間が**タイムスライス**。

  * 例: 10msごとに切り替え

### **3.2 割り込みの瞬間に起きること**

1. プロセスAが `access()` で「ファイルが存在しない」と判断
2. しかし**タイムスライスが切れて**CPUがプロセスBに切り替わる
3. プロセスBが同じファイルを `open(O_CREAT)` で作成
4. 再びプロセスAが実行され、`open()` を実行
5. → Aは「自分が作成した」と誤認してしまう

```
時間 →
┌──────────────┬──────────────┬──────────────┐
| プロセスA      | プロセスB     | プロセスA再開 |
| access(確認)  | open(作成)   | open(再試行)  |
└──────────────┴──────────────┴──────────────┘
               ↑タイムスライス終了 → CPUがAからBに切り替わる
```

これが典型的な**レースコンディション**発生シナリオ。

---

## **4. open(O_CREAT | O_EXCL) で解決できる理由**

* `open(O_CREAT | O_EXCL)` は**存在確認＋新規作成を1回のシステムコールでアトミックに実行**する。
* OSが内部でinodeロックを取り、処理が割り込まれない。
* これによりTOCTOU問題を解消できる。
* ※補足：古いNFS環境では `O_EXCL` が完全に機能しないことがあり、ネットワークファイルシステムでは注意が必要。

---

## **5. アトミック操作とは何か**

* **アトミック**＝「分割されず、一連の操作が他プロセスから見て一瞬で終わる」こと。
* ただし「システムコールだから常にアトミック」というわけではない。

---

## **6. 実験：レースを再現**

ここでは、**2つのプロセスを並列実行**して TOCTOU を意図的に発生させ、その後 `O_CREAT | O_EXCL` で解消されることを確認します。
手元で簡単に再現できるように、**ワンコマンドで並列起動するシェルスクリプト**を用意しました。

---

### 6.1 悪い例：`access()` → `open()`（レースが起きうる）

```c
// race_bad.c
#include <stdio.h>
#include <unistd.h>   // access, usleep
#include <fcntl.h>    // open, O_*
#include <stdlib.h>
#include <sys/stat.h>

int main(void) {
    const char *filename = "race.txt";

    // 存在確認（TOCTOUの"TOC"）
    if (access(filename, F_OK) == -1) {
        // レースが起きやすいよう、意図的にスリープ（10ms）
        usleep(10 * 1000);

        // 作成（"TOU"）。この間に他プロセスが作成し得る
        int fd = open(filename, O_WRONLY | O_CREAT, 0644);
        if (fd == -1) {
            perror("open (bad)");
            exit(1);
        }
        printf("[bad] ファイル作成に成功: %s\n", filename);
        close(fd);
    } else {
        printf("[bad] 既に存在: %s\n", filename);
    }
    return 0;
}
```

---

### 6.2 良い例：`open(O_CREAT | O_EXCL)`（アトミックに解決）

```c
// race_good.c
#include <stdio.h>
#include <unistd.h>
#include <fcntl.h>
#include <errno.h>
#include <stdlib.h>
#include <sys/stat.h>

int main(void) {
    const char *filename = "race.txt";

    // 存在確認＋新規作成を1回のシステムコールで（アトミック）
    int fd = open(filename, O_WRONLY | O_CREAT | O_EXCL, 0644);
    if (fd == -1) {
        if (errno == EEXIST) {
            printf("[good] 既に存在: %s\n", filename);
        } else {
            perror("open (good)");
            exit(1);
        }
    } else {
        printf("[good] ファイル作成に成功: %s\n", filename);
        close(fd);
    }
    return 0;
}
```

---

### 6.3 ビルド手順

```bash
gcc -O2 -Wall -o race_bad  race_bad.c
gcc -O2 -Wall -o race_good race_good.c
```

---

### 6.4 並列実行用シェルスクリプト

```bash
#!/bin/bash
# race_test.sh
# 使い方:
#   ./race_test.sh ./race_bad     # 悪い例（レース発生の可能性）
#   ./race_test.sh ./race_good    # 良い例（排他動作を確認）
# オプション:
#   RUNS=50 ./race_test.sh ./race_bad   # 50回連続で試行（レース再現性UP）

set -euo pipefail

prog=${1:-}
if [[ -z "${prog}" ]]; then
  echo "usage: $0 <program-path>"; exit 2
fi
if [[ ! -x "${prog}" ]]; then
  echo "error: '${prog}' が実行できません"; exit 2
fi

runs=${RUNS:-1}
file="race.txt"

echo ">>> 実行プログラム: ${prog}（${runs}回）"
echo

for i in $(seq 1 "${runs}"); do
  rm -f "${file}"

  # 2つのプロセスを「ほぼ同時」に起動
  "${prog}" & pid1=$!
  "${prog}" & pid2=$!

  wait "${pid1}" "${pid2}" || true

  # 結果を表示
  if [[ -e "${file}" ]]; then
    echo "[run ${i}] 結果: $(ls -l "${file}")"
  else
    echo "[run ${i}] 結果: ファイルなし"
  fi
done
```

> 保存後に実行権限を付与:
> `chmod +x race_test.sh`

---

### 6.5 実行例と観察ポイント

**悪い例（レースが起きうる）**

```bash
./race_test.sh ./race_bad
# 期待される出力例（環境で異なる）:
# [bad] ファイル作成に成功: race.txt
# [bad] ファイル作成に成功: race.txt
# [run 1] 結果: -rw-r--r-- 1 you you 0 ... race.txt
```

* 2プロセスとも「作成に成功」と出るケースがあり、TOCTOUが露呈します。
* 再現性を上げたい場合は `RUNS=50` などで多回数試行してください。

**良い例（排他が効く）**

```bash
./race_test.sh ./race_good
# 期待される出力例（環境で異なる）:
# [good] ファイル作成に成功: race.txt
# [good] 既に存在: race.txt
# [run 1] 結果: -rw-r--r-- 1 you you 0 ... race.txt
```

* 片方だけが作成に成功し、もう一方は `EEXIST` 相当の結果になります。
* `O_CREAT | O_EXCL` により、**存在確認＋作成がアトミック**に処理されたことを体感できます。

---

## **7. 公式ドキュメントで裏付け**

### `open(O_CREAT | O_EXCL)` はアトミック

* **The Open Group / POSIX: `open()`**

  > If **O_CREAT and O_EXCL are set**, open() shall fail if the file exists. **The check for the existence of the file and the creation of the file if it does not exist shall be atomic** with respect to other threads executing open() naming the same filename in the same directory with O_EXCL and O_CREAT set.
https://pubs.opengroup.org/onlinepubs/007904875/functions/open.html?utm_source=chatgpt.com

* **Linux man-pages: `open(2)`**

  > O_EXCL … On **NFS**, O_EXCL is supported only when using NFSv3 or later on kernel 2.6 or later. In NFS environments where O_EXCL support is not provided, programs that rely on it … will contain a **race condition**.
https://man7.org/linux/man-pages/man2/open.2.html

---

## **8. まとめ：タイムスライスとアトミックを意識する**

* タイムスライスによるCPU切り替えが、並列実行環境では必ず起きる。
* その切り替えがレースコンディションの根本原因。
* `open(O_CREAT | O_EXCL)` は、割り込みの隙間をなくす。
* システムコールの設計意図を理解することで、より堅牢なプログラムが書ける。

---

## **本記事で伝えたいこと**

* `open(O_CREAT | O_EXCL)` というフラグをきっかけに、

  * **プロセススケジューリング（タイムスライス）**
  * **レースコンディション**
  * **アトミック操作**
    を体系的に理解できる。

* Linuxプログラミングは、APIの使い方を覚えるだけではなく、**OS内部の仕組みと連動して理解することが重要**。

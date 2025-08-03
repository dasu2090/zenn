---
title: "AWS"
emoji: "📦"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---


**タイトル：**
S3 Transfer Acceleration を有効にしてもアップロードが失敗する問題について

**内容：**
現在、2GBのzipファイルを AWS S3 にアップロードしようとしているのですが、アップロードが途中で止まってしまう問題に直面しています。ネットワークレイテンシが高いことが影響していると考え、`S3 Transfer Acceleration` を有効にしてみましたが、改善が見られませんでした。

試した構成は以下の通りです。

`.aws/config` の内容：

```
[default]
region = us-east-1
output = json
s3 =
    max_concurrent_requests = 10
    max_queue_size = 1000
    multipart_threshold = 64MB
    multipart_chunksize = 64MB
    multipart_max_attempts = 10
    use_accelerate_endpoint = true
```

使用しているコマンドは `aws s3 cp` です。
アップロード対象のバケットには Transfer Acceleration を有効にしており、以下のように `--endpoint-url` は指定していません（`aws-cli` が `use_accelerate_endpoint=true` を認識している想定です）。

また、ping によるネットワーク計測結果は下記の通り、高いレイテンシが発生しています。

```
ping -c 10 s3.amazonaws.com
PING s3.amazonaws.com (52.217.234.24): 56 data bytes
64 bytes from 52.217.234.24: icmp_seq=0 ttl=237 time=210.241 ms
64 bytes from 52.217.234.24: icmp_seq=1 ttl=237 time=337.881 ms
64 bytes from 52.217.234.24: icmp_seq=2 ttl=237 time=212.082 ms
64 bytes from 52.217.234.24: icmp_seq=3 ttl=237 time=272.848 ms
64 bytes from 52.217.234.24: icmp_seq=4 ttl=237 time=210.626 ms
64 bytes from 52.217.234.24: icmp_seq=5 ttl=237 time=231.158 ms
64 bytes from 52.217.234.24: icmp_seq=6 ttl=237 time=215.092 ms
64 bytes from 52.217.234.24: icmp_seq=7 ttl=237 time=224.016 ms
64 bytes from 52.217.234.24: icmp_seq=8 ttl=237 time=218.749 ms
64 bytes from 52.217.234.24: icmp_seq=9 ttl=237 time=211.848 ms

--- s3.amazonaws.com ping statistics ---
10 packets transmitted, 10 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 210.241/234.454/337.881/38.831 ms
```

このような高レイテンシ環境でも S3 Transfer Acceleration によってアップロードの安定性や速度が改善されると期待していましたが、実際には途中で止まってしまうことが多く、転送が成功しません。

**質問：**

1. Transfer Acceleration は高レイテンシのネットワーク環境でも有効に機能するのでしょうか？
2. `aws s3 cp` において Transfer Acceleration の効果を最大限引き出すための追加設定はありますか？
3. 2GB 程度のファイルを安定して転送するための AWS CLI 側・ネットワーク側の対策はあるでしょうか？

アドバイスをいただけると助かります。

---
title: "AWS"
emoji: "😸"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---


## 🔹 タスクステートメント 1.1: データを取り込んで保存する

### 🎓 対象知識

* **データ形式と取り込みメカニズム**:

  * **形式例**: CSV, JSON, Parquet, ORC, Avro, RecordIO
  * **ポイント**:

    * Parquet/ORC：列指向形式、クエリや分析に最適
    * CSV/JSON：行指向、シンプルだが非効率的な場合も
    * RecordIO：SageMaker で高速処理に使われる

* **AWS の主要データソース**:

  * **Amazon S3**：非構造データの保存に最適
  * **Amazon EFS**：共有ファイルストレージ
  * **Amazon FSx for NetApp ONTAP**：高性能なファイルストレージ

* **ストリーミングデータソース**:

  * **Kinesis**, **Apache Kafka**, **Apache Flink**
  * 大量のリアルタイムデータを処理するための取り込みパイプライン構築

* **ストレージオプションのトレードオフ**:

  * S3 は低コスト・高スケーラビリティ、EBS/EFS は高速アクセスに向く

### 🛠 対象スキル

* **データ抽出**:

  * S3 Transfer Acceleration → 高速アップロード
  * EBS プロビジョンド IOPS → 高 I/O パフォーマンス

* **形式選択**:

  * アクセス頻度、スキャン量、処理の複雑さで選ぶ（例：頻繁なクエリには Parquet）

* **SageMaker 連携**:

  * Data Wrangler：GUIベースでデータ準備
  * Feature Store：特徴量を保存・管理

* **データマージ**:

  * AWS Glue/Spark/Pythonなどを使って複数ソース統合

* **容量とスケーラビリティ問題への対応**:

  * ストレージやパーティショニング設計の見直し、メタデータ管理

* **初期考慮事項**:

  * ストレージコスト、レイテンシ、可用性、セキュリティなど

---

## 🔹 タスクステートメント 1.2: データを変換し、特徴量エンジニアリングを実行する

### 🎓 対象知識

* **データクリーニング・変換**:

  * 外れ値処理、欠損補完（平均、中央値など）、重複排除、結合など

* **特徴量エンジニアリング**:

  * スケーリング（MinMax, StandardScaler）
  * ログ変換、ビニング（連続値をカテゴリに分ける）
  * 特徴量の分割（例：日付を年・月・日に分ける）

* **エンコーディング手法**:

  * ワンホット：カテゴリ→バイナリベクトル
  * ラベル：カテゴリ→整数
  * トークン化：テキスト→トークンのリスト

* **可視化・変換ツール**:

  * Data Wrangler（GUI）
  * AWS Glue（ETL）、DataBrew（ノーコード）

* **ストリーミング変換**:

  * AWS Lambda、Apache Spark などでリアルタイム変換

* **アノテーション**:

  * Ground Truth、Amazon Mechanical Turk で高品質なラベルデータ作成

### 🛠 対象スキル

* **AWS ツールを使った変換**:

  * Glue、DataBrew、EMR（Spark）、Data Wrangler などで処理実行

* **Feature Store の活用**:

  * 使い回し可能な特徴量を保存・再利用

* **データ検証・ラベリング**:

  * Ground Truth でセマンティックセグメンテーションやオブジェクト検出用のラベル付けが可能

---

## 🔹 タスクステートメント 1.3: データの完全性を確保し、モデリングに向けてデータを準備する

### 🎓 対象知識

* **バイアスメトリクス**:

  * CI（クラス不均衡）、DPL（ラベルの分布差）など

* **CI への対処**:

  * SMOTEなどの合成データ生成、過/少サンプリング

* **セキュリティ**:

  * 暗号化：SSE-S3, SSE-KMS, CSE
  * 匿名化/マスキング：PII/PHI除去、仮名化

* **コンプライアンス**:

  * GDPR、HIPAA などの規制に準拠

### 🛠 対象スキル

* **データ品質チェック**:

  * Glue Data Quality、DataBrew のプロファイリング機能

* **SageMaker Clarify の使用**:

  * 選択バイアス、測定バイアスを特定し、対策

* **予測バイアス対策**:

  * データの分割、シャッフル、拡張（augmentation）

* **モデルトレーニング用ストレージ設定**:

  * Amazon EFS/FSx → SageMaker のトレーニングジョブで高速読み込み可能

-----

### 1. **Amazon SageMaker 系サービス**

* **SageMaker Studio / Pipelines / Data Wrangler / Feature Store / Ground Truth / Clarify / Canvas** など、SageMaker の各コンポーネントを横断的に活用するシナリオが多数。
* 組み込みアルゴリズム、バイアス検出、特徴量管理、低レイテンシー推論、データ前処理など広範囲あり。

### 2. **データ準備と統合**

* AWS Glue、AWS DMS、Data Wrangler を使ったデータ変換・統合。
* 特にデータ形式（Parquet、RecordIO-Protobufなど）や S3 を中心とした保存場所の選定。

### 3. **分散処理とストリーミング**

* Amazon EMR や PySpark、Streaming での処理（例：EMR で 1TB データを変換、Feature Store にストリーム取り込み）。

### 4. **ベクトルデータベース／生成AI関連（新傾向）**

* ベクトルデータベースを用いた RAG（検索拡張生成）、Amazon Bedrock の知識ベース構築。
* S3ベースの構成選択肢とOpenSearchとの違いなど、設計的理解が必要。

### 5. **機械学習モデル運用（MLOps）**

* Data Drift, Model Bias, Feature Drift などの検出（Clarify / Model Monitor）。
* SageMaker Feature Store の共有・アクセス制御の設計。

### 6. **ラベリングと PII（個人情報）検出**

* Ground Truth / Comprehend / Canvas による PII 検出の自動化。
* Rekognition や Transcribe との適用領域の違い。

---

## 🎯 試験対策のポイント

### 1. **サービス選定の根拠を理解する**

* 類似サービス（例：Glue vs EMR、Pipelines vs Data Wrangler、S3 vs Feature Store）を比較し、**運用コスト・スケーラビリティ・対応形式**で最適解を導けるように。

### 2. **フロー（手順問題）に強くなる**

* ナレッジベースや Feature Store など、**ステップ順問題**が多いため、各サービスの操作フローを把握しておく。

  * 例：S3 → Bedrock ナレッジベース設定 → データ取り込み

### 3. **新サービスへの対応**

* \*\*Bedrock・Canvas・Clarify・Feature Store・VectorDB（Kendra/Opensearch/Athena等）\*\*の使い分け。
* 生成AIやRAG関連は2024年以降の出題範囲として強化されていると予想。

### 4. **ユースケースごとのベストプラクティスを記憶**

* 分類 vs 回帰
* セマンティックセグメンテーションの正しいラベリング手法
* 欠損値処理やデータスケーリング方法（ロバストスケーラーなど）

---

## 📚 おすすめ学習ステップ

| ステップ | 内容                                     | 推奨リソース                                                     |
| ---- | -------------------------------------- | ---------------------------------------------------------- |
| 1    | SageMaker 各機能の使い分け                     | [AWS Skill Builder（無料）](https://explore.skillbuilder.aws/) |
| 2    | Glue、EMR、DMSなどデータパイプライン知識の習得           | \[AWS公式ホワイトペーパー / Blackbelt資料]                             |
| 3    | 過去問や模擬試験で問題演習                          | Udemy / Whizlabs / AWS公式模試                                 |
| 4    | 実機ハンズオン（Data Wrangler や Feature Store） | SageMaker Studio Lab（無料）など活用                               |
| 5    | 最新トレンド対策（生成AI/RAG）                     | [Bedrockハンズオン](https://catalog.workshops.aws/) など          |


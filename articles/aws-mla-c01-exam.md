---
title: "AWS"
emoji: "😸"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---


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


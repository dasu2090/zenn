---
title: "aws"
emoji: "✨"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---

### 傾向：試験で問われるポイント

#### 1. **マルチアカウント戦略が標準**
* **AWS Organizationsが前提:** ほとんどのシナリオで、単一アカウントではなく、複数のアカウントをAWS Organizationsで管理していることが前提となっています。
* [cite_start]**一元管理とガバナンス:** Organizationsの**バックアップポリシー**（問題51 [cite: 6951][cite_start]）、**タグポリシー**（問題38 [cite: 6931, 6932][cite_start]）、そして特に**SCP（サービスコントロールポリシー）**（問題27, 24 [cite: 6913, 6909]）による一元的な統制が頻繁に問われます。OU（組織単位）を適切に設計し、ポリシーを継承させる考え方が重要です。

#### 2. **コスト最適化は「思考の根幹」**
* [cite_start]**単なる値下げではない:** 「最もコスト効率が良い」という問いは、単に安いサービスを選ぶことではありません。**運用オーバーヘッドの削減**（問題6, 25 [cite: 6885, 6910][cite_start]）、**アクセスパターンに応じたS3ストレージクラスの選択**（問題26, 62, 67 [cite: 6911, 6966, 6972][cite_start]）、**予測不能なトラフィックに対する適切な購入オプション**（オンデマンド、リザーブドインスタンス、スポットインスタンス）の選択（問題7 [cite: 6888]）など、多角的な視点が求められます。
* [cite_start]**コストの可視化と予測:** AWS Budgetsの**予測コスト**に基づいたアクション（問題4 [cite: 6882]）など、コストを管理・監視する具体的な方法も問われます。

#### 3. **高可用性とDR（災害対策）は具体的**
* [cite_start]**RTO/RPOの達成:** 「最短の復旧時間（RTO）」「データ損失を最小化（RPO）」といった具体的な目標を、どのサービスの組み合わせで達成するかが問われます。特に、**Amazon Aurora Global Database**（問題14, 19 [cite: 6897, 6903][cite_start]）や**Route 53のフェイルオーバールーティング**（問題70 [cite: 6976]）は重要な選択肢です。
* [cite_start]**部分障害への対応:** システム全体ではなく、一部のコンポーネントが不調になる「部分的障害」にいかに自動で対応するかという、より実践的なシナリオが出題されます（問題1 [cite: 6879]）。**Route 53 Application Recovery Controller**のような高度なサービスも範囲に含まれます。

#### 4. **自動化と疎結合アーキテクチャ**
* [cite_start]**サーバーレスの活用:** Lambda、API Gateway、SQS、EventBridgeなどを組み合わせたサーバーレス・イベント駆動型アーキテクチャは、スケーラビリティと運用負荷削減の観点から頻繁に最適な解決策として登場します（問題9, 23, 54 [cite: 6890, 6908, 6955]）。
* [cite_start]**インフラのコード化（IaC）:** AWS CloudFormation（特にStackSets）を利用したマルチアカウント・マルチリージョンへの一貫したリソース展開が問われます（問題37, 51 [cite: 6930, 6951]）。

#### 5. **セキュリティは「ビルトイン」で考える**
* [cite_start]**最小権限の徹底:** IAMポリシーだけでなく、S3アクセスポイント（問題36 [cite: 6929]）やタスク用のIAMロール（ECS）など、より細かい単位で権限を制御する方法が問われます。
* [cite_start]**プライベート接続の徹底:** 顧客データや機密データを扱うシナリオでは、インターネットを経由しない通信が必須要件となります。**AWS PrivateLink**や**ゲートウェイVPCエンドポイント**の知識は不可欠です（問題28 [cite: 6914]）。
* [cite_start]**統合的なセキュリティ管理:** AWS Security Hub（問題58 [cite: 6960][cite_start]）やAWS Firewall Manager（問題55 [cite: 6957]）を使い、複数のセキュリティサービスからの検出結果やポリシーを組織全体で統合管理する方法が問われます。

---

### 対策：合格に向けた学習戦略

#### 1. **OrganizationsとControl Towerをマスターする**
* SCPの構文（特に`Condition`句）と継承の仕組みを深く理解しましょう。
* AWS Backupポリシーやタグポリシーなど、Organizationsと連携するサービスの一元管理方法をハンズオンで試してみましょう。

#### 2. **コストを「設計要素」として捉える**
* 各サービスの料金体系（例：S3のストレージ料金 vs 取得料金、データ転送料金）を把握し、シナリオに応じて最適な選択ができるようにしましょう。
* 「Savings Plans vs リザーブドインスタンス」「EC2 vs Fargate vs Lambda」など、主要な選択肢のコストメリットとデメリットを比較検討する練習をしてください。

#### 3. **DR戦略をパターン化して覚える**
* 「バックアップ＆リストア」「パイロットライト」「ウォームスタンバイ」「マルチサイト（アクティブ/アクティブ）」の各戦略と、それを実現するAWSサービスの組み合わせ（例：パイロットライト = RDSリードレプリカの昇格）を整理しておきましょう。
* **Route 53 Application Recovery Controller**や**AWS Elastic Disaster Recovery (DRS)**など、最新のDR関連サービスについても概要を把握しておきましょう。

#### 4. **自動化の「引き出し」を増やす**
* 「何かをトリガーにして、自動で何かを実行したい」という要件が出てきたら、EventBridge + Lambda/Step Functions/SQSといったパターンをすぐに思い浮かべられるようにしましょう。
* CloudFormation StackSetsを使って、複数のアカウント・リージョンに同じテンプレートを展開するハンズオンを経験しておくと、設問のイメージが湧きやすくなります。

#### 5. **「なぜそのセキュリティ設定なのか」を説明できるようにする**
* 「なぜここではIAMポリシーではなくSCPなのか？」「なぜVPCピアリングではなくPrivateLinkなのか？」といった、複数の選択肢がある中から特定のセキュリティソリューションを選ぶ理由を論理的に説明できるようにしましょう。
* [cite_start]特に、**S3オブジェクトロック**（問題15 [cite: 6898][cite_start]）によるデータ保護や、**CloudFront OAC**（問題11, 35 [cite: 6893, 6927]）によるS3オリジンへのアクセス制限は頻出の重要パターンです。




### AWS Organizations

1. SCP（Service Control Policy）の使いこなし
- Denyによる制限の使い方（例：特定リージョン、未タグ付け、非バースタブルインスタンスなど）
- AllowのみSCPがデフォルトでは何も制限しない点の理解
- FullAWSAccess SCP を外すことの意味
- 条件キー（StringEquals, Null, aws:RequestTag など）の活用

2. マルチアカウント構成と統制
- OU（組織単位）による管理構造設計
- 各アカウントへのリソース共有（RAM、Control Tower）
- 管理アカウント vs メンバーアカウントの責務分離

3. コスト管理と可視化
- CUR（Cost and Usage Report）+ Athena + QuickSight のパターン
- Savings Plans の全体アカウント最適化とバリエーション
- タグベースのコスト配賦とその統制（Tag Policy、SCP）

4. 監査・ログ管理の中央集約
- CloudTrail Lake の使用（組織単位で管理イベント集約）
- AWS Config + Aggregator のパターン
- CloudTrail Trail の組織単位での集中化構成

5. Control Tower & ガードレール
- Control Tower による自動 OU 構成と制限ルール（proactive / detective）
- 企業ポリシーに合わせた guardrail 適用

6. セキュリティとアイデンティティ統制
- 複数アカウントでのクロスアカウントアクセス（AssumeRole 設計）
- Azure AD や AD FS 連携を IAM Identity Center で実装

⸻

🛠️ 対策と学習ポイント

項目:具体的な対策
SCP の動作原理:Allowだけでは制限されない。明示的なDenyの有効活用を理解しよう。
OUと階層構造:管理の柔軟性を持たせたOU設計パターンを理解（例：Prod/Dev分離）
Resource Access Manager (RAM):トランジットゲートウェイやVPC共有にRAMをどう使うか明確に理解
Control Tower:ガードレールの設計（Tag強制, EC2制限, リージョン制限）を実践で学ぶ
コスト制御:Savings Plan, Cost Explorer, CUR + Athenaの組み合わせパターンを暗記レベルに
CloudTrail Lake:管理アカウントにおける統合ログ設計とクエリパターン理解
タグ戦略:Tag Policy, 強制付与と準拠チェックの仕組みを設計できるように
IAM Identity Center (旧SSO):Azure ADやID連携の構成と、組織アカウントへのアクセス戦略理解


⸻

🧠 試験対策として特に重要なトピックまとめ

トピック	理解レベルの指標
SCPとTag Policyの併用	⭐⭐⭐⭐
Control TowerとLanding Zoneの構築	⭐⭐⭐⭐
コスト最適化の戦略設計（Savings Plan/RI）	⭐⭐⭐⭐
CloudTrail Lakeとセキュリティ統制	⭐⭐⭐⭐
RAMによるVPC/TGW共有とパターン選定	⭐⭐⭐
IAM Identity Center + AzureAD連携	⭐⭐⭐
アカウント移動・招待フロー（API含む）	⭐⭐⭐

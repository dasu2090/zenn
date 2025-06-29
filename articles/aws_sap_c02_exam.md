---
title: "aws"
emoji: "✨"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---


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

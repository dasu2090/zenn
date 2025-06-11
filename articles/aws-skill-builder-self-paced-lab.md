---
title: "aws skill builder self paced lab"
emoji: "👻"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["aws"]
published: false
---

6/6 レイアウトが変わった

インスタンスクラス
IAM拒否
db.t3.medium

RDPのURLでアクセスできない
Systems Manager → フリートマネージャー → リモートデスクトップ
![](https://storage.googleapis.com/zenn-user-upload/d9602df03776-20250501.png =600x)

アクセス権がない
![](https://repost.aws/questions/QU4Eixq-mdTbKI7cKWNJdf4g/aws-skill-builder-self-paced-lab-content-not-accessible)

## 基礎

### 30分

[**Lab - Building a Serverless API (日本語)**](https://explore.skillbuilder.aws/learn/courses/21696/lab-building-a-serverless-api-ri-ben-yu)
AWS SAMを使用してサーバーレスアプリケーションをデプロイします。AWS LambdaからAmazon S3 オブジェクトのコンテンツを読み取る関数を実装するプロセスを学習します。
$\textcolor{green}{tag}$: AWS Cloud9, Amazon S3, AWS CloudFormation


[**Using AWS CloudFormation for Automation (日本語)**](https://explore.skillbuilder.aws/learn/courses/21789/lab-using-aws-cloudformation-for-automation-ri-ben-yu)
CloudFormation テンプレートを確認することから始め、Amazon EC2インスタンスでnginxが実行されていることを確認します。AWS CLIを使ってEC2インスタンスを起動するCloudFormationスタックを作成します。ユーザーデータでnginxをインストールし、ブラウザでnginxの動作を確認することで、CloudFormationによる自動化を学習します。
$\textcolor{green}{tag}$: AWS CloudFormation, Amazon Elastic Compute Cloud (EC2), 
AWS Command Line Interface (CLI)


[**Integrating Amazon Simple Queue Service (Amazon SQS) (日本語)**](https://explore.skillbuilder.aws/learn/courses/21371/lab-integrating-amazon-simple-queue-service-amazon-sqs-ri-ben-yu)
2つのPythonスクリプト（受信と送信）を用いてAmazon SQSの基本的な操作を体験します。コンソールとAWS CLIでSQSキューを確認し、受信スクリプトを実行してメッセージをリッスン、送信スクリプトのメッセージをキューに送信する手順を学びます。
$\textcolor{green}{tag}$: Amazon Simple Queue Service (SQS), AWS Cloud9, AWS Command Line Interface (CLI)


[**Walkthrough of the AWS Well-Architected Tool (日本語)**](https://explore.skillbuilder.aws/learn/courses/16491/walkthrough-of-the-aws-well-architected-tool-ri-ben-yu)
AWS Well-Architected Toolを用いてアプリケーションアーキテクチャを評価する手順を学習します。ワークロードの作成、レビューの実施、マイルストーンの保存、およびマイルストーンレポートの表示を通して、アーキテクチャの改善点とベストプラクティスを学びます。
$\textcolor{green}{tag}$: AWS Well-Architected Tool


[**Lab - Create a Static Website with Amazon Simple Storage Service (Amazon S3) (日本語)**](https://explore.skillbuilder.aws/learn/courses/21878/lab-create-a-static-website-with-amazon-simple-storage-service-amazon-s3-ri-ben-yu)
Amazon S3を使用して静的なウェブサイトを作成し、パブリックアクセスを許可するためのバケットポリシーを設定します。HTMLファイルを作成・アップロードし、ウェブサイトのエンドポイントを通じてアクセスをテストする手順を学びます。
$\textcolor{green}{tag}$: Amazon Simple Storage Service (S3)


[**Lab - Integrating Amazon DynamoDB (日本語)**](https://explore.skillbuilder.aws/learn/courses/21336/lab-integrating-amazon-dynamodb-ri-ben-yu)
#ラボを開始するとなぜか学習ダッシュボードのホームに戻るため受講できませんでした。


### 40分

[**Lab - AWS CodeBuild Hello World (日本語)**](https://explore.skillbuilder.aws/learn/courses/21814/lab-aws-codebuild-hello-world-ri-ben-yu)
AWS CodeBuildの主要機能と特徴を理解し、CodeCommitリポジトリと連携したJavaアプリケーションの自動ビルドプロセスを体験します。buildspec.ymlの確認、CodeBuildプロジェクトの実行、生成されたJARファイルのローカル実行を通して、CI/CDパイプラインの基礎を学びます。
$\textcolor{green}{tag}$: AWS CodeBuild, AWS CodeCommit, Amazon Simple Storage Service (S3), AWS Cloud9


### 45分

[**Introduction to Amazon EC2 Auto Scaling (日本語)**](https://explore.skillbuilder.aws/learn/courses/7475/introduction-to-amazon-ec2-auto-scaling-ri-ben-yu)
Amazon EC2 Auto Scalingの概要の確認と、起動テンプレート作成、Auto Scalingグループ作成、起動確認、Auto Scalingの基本を習得します。
$\textcolor{green}{tag}$: Amazon EC2


[**Introduction to Amazon DynamoDB (日本語)**](https://explore.skillbuilder.aws/learn/courses/7493/introduction-to-amazon-dynamodb-ri-ben-yu)
Amazon DynamoDBの基本的な操作を学びます。テーブルの作成、データの追加と変更、プライマリキーを用いた効率的なクエリ、そしてテーブルの削除といった一連の流れを体験します。
$\textcolor{green}{tag}$: Amazon DynamoDB


[**Introduction to AWS CloudFormation (日本語)**](https://explore.skillbuilder.aws/learn/courses/7756/introduction-to-aws-cloudformation-ri-ben-yu)
AWS CloudFormationを用いて定義済みのテンプレートからWordPressとMySQLが動作するEC2インスタンスを含むスタックを作成し、パラメータ、リソース、出力を確認します。
$\textcolor{green}{tag}$: AWS CloudFormation


[**Introduction to Amazon Virtual Private Cloud (VPC) (日本語)**](https://explore.skillbuilder.aws/learn/courses/7495/introduction-to-amazon-virtual-private-cloud-vpc-ri-ben-yu)
Amazon VPCウィザードを用いてVPCを作成し、インターネットゲートウェイのアタッチ、サブネットの追加、ルーティング設定を通して、VPCの基本的なコンポーネント（パブリック/プライベートサブネット、ルートテーブル、NATゲートウェイ、ネットワークACL）について学習します。
$\textcolor{green}{tag}$: Amazon Virtual Private Cloud (VPC)


[**Introduction to AWS Identity and Access Management (IAM) (日本語)**](https://explore.skillbuilder.aws/learn/courses/7487/introduction-to-aws-identity-and-access-management-iam-ri-ben-yu)
AWS IAMの基本的な概念と操作を学習します。事前に作成されたユーザー、グループ、ポリシーを確認し、シナリオに基づいてユーザーをグループに追加し、IAMサインインURLを使用して各ユーザーのアクセス許可をテストします。
$\textcolor{green}{tag}$: AWS Identity and Access Management (IAM)


[**Using Open Data with Amazon S3 (日本語)**](https://explore.skillbuilder.aws/learn/courses/8591/using-open-data-with-amazon-s3-ri-ben-yu)
Amazon S3にデータをアップロードし、バケットポリシーとCORS設定でアクセス許可を設定、静的ウェブサイトホスティング機能で公開します。JavaScriptを用いてS3バケットのコンテンツをウェブページに動的に表示する方法を学習します。
tag: Amazon S3


[**Introduction to AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/7502/introduction-to-aws-lambda-ri-ben-yu)
イベント駆動型のAWS Lambdaの基本を学び、S3への画像アップロードをトリガーに画像のサムネイルを自動生成するLambda関数を作成します。S3をイベントソースとして設定し、CloudWatch LogsでLambda関数の実行状況をモニタリングします。
tag: AWS Lambda, Amazon CloudWatch, Amazon S3


#### メンテナンス中
[**Introduction to AWS CloudFormation Designer (日本語)**](https://explore.skillbuilder.aws/learn/courses/10977/introduction-to-aws-cloudformation-designer-ri-ben-yu)


[**Introduction to Amazon ElastiCache with Windows Server (日本語)**](https://explore.skillbuilder.aws/learn/courses/8582/introduction-to-amazon-elasticache-with-windows-server-ri-ben-yu)


### 1時間

[**Analyze Big Data with Hadoop (日本語)**](https://explore.skillbuilder.aws/learn/courses/6936/analyze-big-data-with-hadoop-ri-ben-yu) 
※「このラボは 日本語 ではまだ利用できません。」と表示されて英語表記となっています。
Amazon EMRを使用してHadoopクラスターを起動し、HiveQLスクリプトでログデータを処理して分析する方法を学びます。処理結果はAmazon S3に保存され、ダウンロードして確認したり、Hive CLIから直接クエリを実行して表示を確認します。
:::details 注意点
「**EMR クラスター CLI に接続し、HiveQL を使用してクエリを実行する**」項目において、**ターミナルのロケール（文字コード）が ASCII に設定されています。**
```'ascii' codec can't encode characters …```
EMR クラスター名やタグなどに **非ASCII文字（日本語や絵文字など）** が入っていると、ASCII 環境ではうまく処理できずエラーになるため、**ターミナルで UTF-8 を使うように環境変数を設定が必要です。**
```
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8
```
:::

[**Introduction to Amazon EC2 (日本語)**](https://explore.skillbuilder.aws/learn/courses/7506/introduction-to-amazon-ec2-ri-ben-yu)
Amazon EC2インスタンスの起動、サイズ変更、管理、モニタリングの概要を学びます。インスタンスの終了保護、セキュリティグループの設定、インスタンスタイプの変更、EBSボリュームの調整を通じてEC2インスタンスの基本的な操作を体験します。
$\textcolor{green}{tag}$: Amazon Elastic Compute Cloud (EC2)


[**Introduction to Amazon Aurora (日本語)**](https://explore.skillbuilder.aws/learn/courses/9032/introduction-to-amazon-aurora-ri-ben-yu)
MySQL互換の高性能フルマネージドデータベースエンジンであるAmazon Auroraの学習です。Auroraインスタンスの作成と接続、既存のMySQLインスタンスとの比較、データロード、そしてクエリ実行を通してAuroraの基本的な使用方法を学びます。
tag: Amazon Aurora, Amazon RDS for MySQL, Amazon EC2, AWS Systems Manager


[**Introduction to Amazon ElastiCache (日本語)**](https://explore.skillbuilder.aws/learn/courses/8597/introduction-to-amazon-elasticache-ri-ben-yu)
ウェブアプリケーションのパフォーマンス向上に役立つインメモリキャッシュサービスであるAmazon ElastiCacheについて学びます。Redisエンジンを用いたElastiCacheクラスターの作成、EC2インスタンスからの接続とコマンド実行、そしてリソースのクリーンアップを行います。
tag: Amazon ElastiCache (Redis), Amazon EC2


[**Introduction to Amazon Relational Database Service (RDS) (Linux) (日本語)**](https://explore.skillbuilder.aws/learn/courses/8593/introduction-to-amazon-relational-database-service-rds-linux-ri-ben-yu)
Amazon RDSによるMySQLインスタンスの作成、Session Managerによる接続、テーブル作成、データ操作、そしてクエリ実行の一連の流れを体験します。
tag: Amazon Relational Database Service (RDS), AWS Systems Manager (Session Manager), Amazon EC2


[**Introduction to Amazon Relational Database Service (RDS) (Windows) (日本語)**](https://explore.skillbuilder.aws/learn/courses/7491/introduction-to-amazon-relational-database-service-rds-windows-ri-ben-yu)


[**Lab - Using the AWS CLI for Automation (日本語)**](https://explore.skillbuilder.aws/learn/courses/21773/lab-using-the-aws-cli-for-automation-ri-ben-yu)


[**Introduction to Amazon CloudFront (日本語)**](https://explore.skillbuilder.aws/learn/courses/7498/introduction-to-amazon-cloudfront-ri-ben-yu)


[**Serverless Web Apps using Amazon DynamoDB - Part 1 (日本語)**](https://explore.skillbuilder.aws/learn/courses/7504/serverless-web-apps-using-amazon-dynamodb-part-1-ri-ben-yu)


[**Serverless Web Apps using Amazon DynamoDB - Part 2 (日本語)**](https://explore.skillbuilder.aws/learn/courses/8599/serverless-web-apps-using-amazon-dynamodb-part-2-ri-ben-yu)


[**Serverless Web Apps using Amazon DynamoDB - Part 3 (日本語)**](https://explore.skillbuilder.aws/learn/courses/8601/serverless-web-apps-using-amazon-dynamodb-part-3-ri-ben-yu)


[**Working with AWS CodeCommit (日本語)**](https://explore.skillbuilder.aws/learn/courses/7480/working-with-aws-codecommit-ri-ben-yu)


[**Creating an Amazon Virtual Private Cloud (VPC) with AWS CloudFormation (日本語)**](https://explore.skillbuilder.aws/learn/courses/9636/creating-an-amazon-virtual-private-cloud-vpc-with-aws-cloudformation-ri-ben-yu)
#このラボは 日本語 ではまだ利用できません。

[**Introduction to Amazon API Gateway (日本語)**](https://explore.skillbuilder.aws/learn/courses/7485/introduction-to-amazon-api-gateway-ri-ben-yu)


[**Lab - Using the AWS Systems Manager Run Command for Automation (日本語)**](https://explore.skillbuilder.aws/learn/courses/21968/lab-using-the-aws-systems-manager-run-command-for-automation-ri-ben-yu)


[**Introduction to Elastic Load Balancing (日本語)**](https://explore.skillbuilder.aws/learn/courses/7489/introduction-to-elastic-load-balancing-ri-ben-yu)


[**Working with Elastic Load Balancing (日本語)**](https://explore.skillbuilder.aws/learn/courses/10973/working-with-elastic-load-balancing-ri-ben-yu)


[**Getting Started with Amazon Comprehend: Custom Entity Recognition (日本語)**](https://explore.skillbuilder.aws/learn/courses/15261/getting-started-with-amazon-comprehend-custom-entity-recognition-ri-ben-yu)


[**Introduction to Amazon Simple Storage Service (S3) (日本語)**](https://explore.skillbuilder.aws/learn/courses/7508/introduction-to-amazon-simple-storage-service-s3-ri-ben-yu)


[**Introduction to AWS Key Management Service (日本語)**](https://explore.skillbuilder.aws/learn/courses/7500/introduction-to-aws-key-management-service-ri-ben-yu)


[**Introduction to Amazon Elastic Block Store (Amazon EBS) (日本語)**](https://explore.skillbuilder.aws/learn/courses/12405/introduction-to-amazon-elastic-block-store-amazon-ebs-ri-ben-yu)


[**Evolution of a Website: Going from Single Server to Serverless (日本語)**](https://explore.skillbuilder.aws/learn/courses/21886/evolution-of-a-website-going-from-single-server-to-serverless-ri-ben-yu)


[**Performing a Basic Audit of your AWS Environment (日本語)**](https://explore.skillbuilder.aws/learn/courses/6928/performing-a-basic-audit-of-your-aws-environment-ri-ben-yu)


[**Traffic Monitoring and Packet Analysis (日本語)**](https://explore.skillbuilder.aws/learn/courses/16762/traffic-monitoring-and-packet-analysis-ri-ben-yu)


[**Hosting WordPress Using Amazon S3 (日本語)**](https://explore.skillbuilder.aws/learn/courses/8589/hosting-wordpress-using-amazon-s3-ri-ben-yu)


[**Using AWS Lambda with Amazon CloudWatch and SNS to Implement a Slack Chat Bot (日本語)**](https://explore.skillbuilder.aws/learn/courses/7758/using-aws-lambda-with-amazon-cloudwatch-and-sns-to-implement-a-slack-chat-bot-ri-ben-yu)


[**Introduction to Amazon Elastic Container Registry (日本語)**](https://explore.skillbuilder.aws/learn/courses/6934/introduction-to-amazon-elastic-container-registry-ri-ben-yu)
Amazon Elastic Container Registry (ECR) を使用してコンテナ化されたウェブアプリケーションのイメージを保存、管理、デプロイする方法を学びます。ECRリポジトリの作成、Dockerイメージのプッシュ、Amazon Elastic Container Service (ECS)へのアプリケーションデプロイを通じてコンテナワークフローを実践します。
tag: Amazon Elastic Container Registry (Amazon ECR), Amazon Elastic Container Service (Amazon ECS)


[**Working with Amazon Elastic Container Service (日本語)**](https://explore.skillbuilder.aws/learn/courses/6926/working-with-amazon-elastic-container-service-ri-ben-yu)
アクセス権が無い


[**Securing VPC Resources with Security Groups (日本語)**](https://explore.skillbuilder.aws/learn/courses/13855/securing-vpc-resources-with-security-groups-ri-ben-yu)
メンテナンス


### 1時間15分

[**Introduction to Amazon Redshift**](https://explore.skillbuilder.aws/learn/courses/6932/introduction-to-amazon-redshift-ri-ben-yu)


[**Introduction to Amazon Relational Database Service (RDS) - SQL Server
db.t3.medium**](https://explore.skillbuilder.aws/learn/courses/8603/introduction-to-amazon-relational-database-service-rds-sql-server-ri-ben-yu)
Microsoft SQL Server Management Studio から RDS インスタンスにアクセスする
SSL証明書の信頼性が原因
“Trust server certificate”チェックする
![](https://storage.googleapis.com/zenn-user-upload/ad1c7ece16ec-20250501.png =400x)
![](https://storage.googleapis.com/zenn-user-upload/7e8688dab0d9-20250501.png =400x)


[**Building BI Dashboards with Amazon QuickSight**](https://explore.skillbuilder.aws/learn/courses/18250/building-bi-dashboards-with-amazon-quicksight-ri-ben-yu)

[**Getting Started with Amazon Comprehend: Custom Classification (日本語)**](https://explore.skillbuilder.aws/learn/courses/15277/getting-started-with-amazon-comprehend-custom-classification-ri-ben-yu)

[**Serverless Architectures using Amazon CloudWatch Events and Scheduled Events with AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/7760/serverless-architectures-using-amazon-cloudwatch-events-and-scheduled-events-with-aws-lambda-ri-ben-yu)


### 2時間
[**Building VPC, S3, EC2, and RDS Products with AWS Service Catalog (日本語)**]()
not yet


## 中級

### 30分
[**Building your First Quantum Circuit with Amazon Braket (日本語)**](https://explore.skillbuilder.aws/learn/courses/17467/building-your-first-quantum-circuit-with-amazon-braket-ri-ben-yu)

### 1時間
[**Launching Amazon EC2 Instances (日本語)**](https://explore.skillbuilder.aws/learn/courses/15432/launching-amazon-ec2-instances-ri-ben-yu)

[**A Day in the Life of a Data Engineer (日本語)**](https://explore.skillbuilder.aws/learn/courses/16319/a-day-in-the-life-of-a-data-engineer-ri-ben-yu)

[**Working with Amazon Redshift (日本語)**](https://explore.skillbuilder.aws/learn/courses/8580/working-with-amazon-redshift-ri-ben-yu)

[**Deploying Your First AWS Lambda Container (日本語)**](https://explore.skillbuilder.aws/learn/courses/13299/deploying-your-first-aws-lambda-container-ri-ben-yu)



[**EC2 Instance Rightsizing (日本語)**](https://explore.skillbuilder.aws/learn/courses/18130/ec2-instance-rightsizing-ri-ben-yu)
EC2インスタンスの適切なサイジングによるコスト最適化を体験します。CloudWatchエージェントの導入、負荷シミュレーション、メトリクス分析に基づき、インスタンスタイプやサイズを変更し、将来的なリソース制約を監視するためのCloudWatchアラームを設定します。
$\textcolor{green}{tag}$: Amazon Elastic Compute Cloud (EC2), Amazon CloudWatch, AWS Systems Manager, AWS Pricing Calculator


[**EMR File System Client-side Encryption Using AWS KMS-managed Keys (日本語)**](https://explore.skillbuilder.aws/learn/courses/6935/emr-file-system-client-side-encryption-using-aws-kms-managed-keys-ri-ben-yu)
EMR File System(EMRFS)を使用してAmazon S3に保存されるデータに対して、AWS KMSで管理されたキーによるクライアント側の保管時の暗号化を有効にする方法を学びます。EMRクラスターの作成、セキュリティ設定、S3への暗号化されたデータの書き込みと読み取り、そして直接S3からのデータの確認を行います。
tag: Amazon EMR, AWS Key Management Service (KMS), Amazon S3, Amazon EC2


[**Maintaining High Availability with Auto Scaling (日本語)**](https://explore.skillbuilder.aws/learn/courses/6925/maintaining-high-availability-with-auto-scaling-ri-ben-yu)
Auto Scalingを活用して高可用性を維持する方法を学びます。起動テンプレートとAuto Scalingグループを作成し、負荷に応じてEC2インスタンスが自動的にスケールアップ・ダウンするポリシーと通知を設定し、その動作を検証します。
tag: Amazon EC2 Auto Scaling, Amazon EC2, Elastic Load Balancing (ELB), Amazon CloudWatch, Amazon Simple Notification Service (SNS), AWS Command Line Interface (CLI)


[**Building Highly Available Web Application (日本語)**](https://explore.skillbuilder.aws/learn/courses/16212/building-highly-available-web-application-ri-ben-yu)
CloudFormationを用いて複数のアベイラビリティーゾーンに分散した高可用性ウェブアプリケーションを構築します。VPC、RDS、ElastiCache、EFS、Auto Scaling、ロードバランサーなどのAWSサービスを連携させ、耐障害性とスケーラビリティを備えたWordPress環境をデプロイし、Fault Injection Simulatorによるカオステストを通じてその可用性を検証します。
tag: AWS CloudFormation, Amazon Virtual Private Cloud (VPC), Amazon Relational Database Service (RDS), Amazon Aurora, Amazon ElastiCache for Memcached, Amazon Elastic File System (EFS), Amazon Elastic Compute Cloud (EC2), Auto Scaling, Application Load Balancer (ALB), AWS Fault Injection Simulator (FIS)



[**Migrating RDS MySQL to Aurora with Read Replica (日本語)**](https://explore.skillbuilder.aws/learn/courses/16645/migrating-rds-mysql-to-aurora-with-read-replica-ri-ben-yu)
Amazon RDS MySQLから高可用性なAmazon Aurora MySQLクラスターへの移行手順を学習します。Auroraリードレプリカの作成と昇格、フェイルオーバー優先度の設定、そして手動フェイルオーバーの実行を通して、データベースの移行と耐障害性を高める方法を習得します。
tag: Amazon Relational Database Service (RDS), Amazon Aurora, Amazon Elastic Compute Cloud (EC2)


[**Lab - Build a Product Recommendation Engine using Amazon Neptune (日本語)**](https://explore.skillbuilder.aws/learn/courses/22036/lab-build-a-product-recommendation-engine-using-amazon-neptune-ri-ben-yu)
リレーショナルデータベースの顧客、注文、商品などのデータをAmazon Neptuneのグラフ構造にモデル化し、商品レコメンデーションエンジンを構築します。顧客の購入履歴、世帯情報、商品の評価といった複数のデータソースを統合し、より関連性の高い推奨をリアルタイムで提供する方法を学びます。
tag: Amazon Neptune, Amazon SageMaker


[**Effortless Relational Scalability with Amazon Aurora Serverless v2 (日本語)**](https://explore.skillbuilder.aws/learn/courses/16225/effortless-relational-scalability-with-amazon-aurora-serverless-v2-ri-ben-yu)
Amazon Aurora Serverless v2 for PostgreSQLを設定し、pgbenchによる負荷テストを通じてワークロードの変化に応じた自動スケーリングを検証します。CloudWatchダッシュボードとPerformance Insightsを用いてデータベースのパフォーマンスとスケーリングの様子をモニタリングします。
tag: Amazon Aurora, Amazon CloudWatch, Amazon RDS Performance Insights, AWS Cloud9, AWS CloudFormation


[**Amazon DynamoDB CRUD Activities Using the AWS CLI and SDK (日本語)**](https://explore.skillbuilder.aws/learn/courses/8617/amazon-dynamodb-crud-activities-using-the-aws-cli-and-sdk-ri-ben-yu)
AWS CLIとAWS SDK for Python (Boto3) を使用してAmazon DynamoDBテーブルを作成、データのCRUD操作（作成、読み取り、更新、削除）を実行する方法を学習します。DynamoDBの基本的な操作と、CLIとSDKそれぞれの使用方法を習得します。
tag: Amazon DynamoDB, AWS Command Line Interface (CLI), AWS SDK for Python (Boto3), AWS Cloud9


[**Amazon DynamoDB Capacity Sizing (日本語)**](https://explore.skillbuilder.aws/learn/courses/8621/amazon-dynamodb-capacity-sizing-ri-ben-yu)
Amazon DynamoDBのプロビジョンドキャパシティーモードにおけるスループット性能の管理、CloudWatchによるパフォーマンス監視、Auto Scalingによる動的なキャパシティー調整、そしてオンデマンドキャパシティーモードへの移行について学習します。AWS SDK for Python (Boto3) を用いて、テーブルのキャパシティー設定を変更し、パフォーマンスへの影響を検証します。
tag: Amazon DynamoDB, Amazon CloudWatch, AWS SDK for Python (Boto3), AWS Cloud9


[**Amazon DynamoDB - Monitoring (日本語)**](https://explore.skillbuilder.aws/learn/courses/8625/amazon-dynamodb-monitoring-ri-ben-yu)
Amazon DynamoDBのモニタリングについて学習します。CloudWatchアラームの作成と管理、CloudWatch Contributor Insightsの活用、運用データ可視化のためのCloudWatchダッシュボード構築、そしてパフォーマンス問題のトラブルシューティングに役立つAWS X-Rayの使用方法を習得します。
tag: Amazon DynamoDB, Amazon CloudWatch, AWS X-Ray, AWS Lambda


[**Amazon DynamoDB Scans, Queries, and Indexes (日本語)**](https://explore.skillbuilder.aws/learn/courses/8619/amazon-dynamodb-scans-queries-and-indexes-ri-ben-yu)
Amazon DynamoDBにおけるデータの検索方法（スキャンとクエリ）、効率的なデータ取得のためのローカルセカンダリインデックス（LSI）とグローバルセカンダリインデックス（GSI）の作成と利用について学習します。Python用AWS SDK (Boto3) を使用して、これらの操作を実行し、パフォーマンスの違いを比較します。
tag: Amazon DynamoDB, AWS Cloud9, AWS SDK for Python (Boto3)


[**Amazon DynamoDB Streams and TTL (日本語)**](https://explore.skillbuilder.aws/learn/courses/8623/amazon-dynamodb-streams-and-ttl-ri-ben-yu)
Amazon DynamoDB StreamsとTTL（Time To Live）を活用し、データベースの変更をトリガーにしたイベント通知や、有効期限切れデータの自動アーカイブを行う方法を学習します。AWS CLI、AWS Lambda、Amazon SNS、Amazon S3などのサービスを連携させ、イベント駆動型のワークフローを構築します。
tag: Amazon DynamoDB, AWS Lambda, Amazon SNS, Amazon S3, AWS Cloud9, AWS CLI


[**My Bucket, My Rules (日本語)**](https://explore.skillbuilder.aws/learn/courses/15735/my-bucket-my-rules-ri-ben-yu)
Amazon S3バケットのセキュリティを強化するためのバケットポリシー設定について学習します。HTTPS接続の強制、VPCエンドポイント経由のアクセス制限、特定の暗号化オプションとKMSキーによるオブジェクトアップロードの適用方法をAWS CLIを用いて実践します。
tag: Amazon S3, AWS CLI


[**Automating AWS Services with Scripting and the AWS CLI (日本語)**](https://explore.skillbuilder.aws/learn/courses/10975/automating-aws-services-with-scripting-and-the-aws-cli-ri-ben-yu)
AWSマネジメントコンソール、AWS CLI、AWS SDK (Python) を使用してAWSサービスを操作し、EC2インスタンスの管理、S3バケットへのファイル操作、EBSスナップショットの自動化、CloudWatchカスタムメトリクスの送信といった自動化について学びます。また、AWS Systems Manager Session ManagerによるEC2インスタンスへの安全な接続方法と、IAMロールを利用したセキュリティ認証情報管理についても習得します。
tag: AWS Systems Manager (Session Manager), AWS CLI, AWS SDK for Python (Boto3), Amazon EC2, Amazon S3, Amazon EBS, Amazon CloudWatch


[**AWS Federated Authentication with AD FS (日本語)**](https://explore.skillbuilder.aws/learn/courses/10979/aws-federated-authentication-with-ad-fs-ri-ben-yu)
AD FSとAWS IAMを連携させて、Active DirectoryユーザーがSAML認証を通じてAWSマネジメントコンソールへフェデレーションアクセスする方法を学びます。AD FSサーバーのセットアップ、Active Directoryグループとユーザーの作成、IAMでのIDプロバイダーと信頼ポリシーの設定を行い、アクセス制限が正しく機能するかを検証します。
tag: AWS Identity and Access Management (IAM), Amazon Elastic Compute Cloud (EC2), AWS Systems Manager (Fleet Manager)


[**Troubleshooting API Gateway with Lambda Proxy Integration (日本語)**](https://explore.skillbuilder.aws/learn/courses/17004/troubleshooting-api-gateway-with-lambda-proxy-integration-ri-ben-yu)
API GatewayとLambdaプロキシ統合で発生する「内部サーバーエラー (500)」のトラブルシューティングを行い、「Hello from Lambda (200)」を返すように修正します。CloudWatch Logsでエラーを特定し、API GatewayのLambda関数統合設定とLambda関数のコード（Python）の修正を通じて問題を解決します。
tag: Amazon API Gateway, AWS Lambda, Amazon CloudWatch Logs, AWS Identity and Access Management (IAM)


[**Launching and Managing a Web Application with AWS CloudFormation (日本語)**](https://explore.skillbuilder.aws/learn/courses/7740/launching-and-managing-a-web-application-with-aws-cloudformation-ri-ben-yu)
AWS CloudFormationを使ってウェブアプリケーションをプロビジョニングし管理する方法を学習します。S3バケットの作成と保持ポリシーの確認から始まり、EC2インスタンス上のシンプルなPHPウェブアプリケーションのデプロイ、既存スタックのリソース（インスタンスタイプ、タグ、IAMロール）の変更、そしてAuto ScalingとElastic Load Balancingによる高可用性構成への変換までを実践します。
tag: AWS CloudFormation, Amazon S3, Amazon EC2, Auto Scaling, Elastic Load Balancing (ELB)


[**.NET Workloads on AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/16237/net-workloads-on-aws-lambda-ri-ben-yu)
AWS Cloud9と.NET CLIを使用して、.NETアプリケーションをAWS Lambdaにデプロイし、変更、呼び出す方法を学びます。サーバーレスASP.NETウェブアプリケーションの構築、Amazon S3バケットリストを取得するLambda関数の作成、そしてそれらの呼び出しを実践します。
tag: AWS Cloud9, AWS Lambda, Amazon S3, AWS Serverless Application Model (SAM) 


[**Building with Amazon Aurora Databases (日本語)**](https://explore.skillbuilder.aws/learn/courses/16587/building-with-amazon-aurora-databases-ri-ben-yu)
Amazon Aurora (MySQL互換) のパラレルクエリ機能について学習し、大規模なデータセットに対するクエリパフォーマンスへの影響を理解します。異なるインスタンスサイズでのパラレルクエリの動作を比較し、その活用方法を実践します。
tag: Amazon Aurora, Amazon Elastic Compute Cloud (EC2), Amazon CloudWatch


[**AWS Network Firewall Fundamentals (日本語)**](https://explore.skillbuilder.aws/learn/courses/17056/aws-network-firewall-fundamentals-ri-ben-yu)
AWS Network Firewall を使用して、組織の VPC におけるネットワークセキュリティのセットアップとデプロイを学びます。基本的なネットワークアーキテクチャから始め、トラフィック検査とフィルタリングのために Network Firewall を設定し、最終的に NAT ゲートウェイを含むより高度なアーキテクチャでルーティングをテストします。
tag: AWS Network Firewall, Amazon EC2, AWS Systems Manager Session Manager, Amazon VPC


[**Update Security Groups Automatically Using AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/7764/update-security-groups-automatically-using-aws-lambda-ri-ben-yu)
AWS Lambdaを使用してAWS IPアドレスの範囲変更に自動的に対応し、Amazon VPCセキュリティグループを更新する方法を学びます。これにより、CloudFrontやAWS WAFからのトラフィックのみを許可することでウェブアプリケーションのセキュリティを強化します。
tag: AWS Lambda, Amazon VPC (セキュリティグループ), Amazon EC2


[**Securing the Endpoint (日本語)**](https://explore.skillbuilder.aws/learn/courses/14298/securing-the-endpoint-ri-ben-yu)
EC2インスタンス、保管中のデータ、転送中のデータを保護するためのセキュリティ対策を実践します。カスタムAMIの作成、Systems Managerによるパッチ適用、EBS暗号化、セキュリティグループルールの設定を通じて、エンドポイントセキュリティを強化します。
tag: Amazon EC2, AWS Systems Manager (パッチマネージャー、セッションマネージャー), Amazon EBS, Amazon VPC


[**Lab - Troubleshooting - IAM Access Issues (日本語)**](https://explore.skillbuilder.aws/learn/courses/18458/lab-troubleshooting-iam-access-issues-ri-ben-yu)
IAMロールの引き受けに関する問題に焦点を当て、IAMユーザーのアイデンティティベースポリシーとIAMロールの信頼ポリシーを最小権限の原則に基づいて修正し、問題を解決する方法を学びます。
tag: AWS Identity and Access Management (IAM), AWS Systems Manager (Session Manager)


[**Managing Access to Amazon S3 Resources with Amazon VPC Endpoints (日本語)**](https://explore.skillbuilder.aws/learn/courses/11541/managing-access-to-amazon-s3-resources-with-amazon-vpc-endpoints-ri-ben-yu)
Amazon VPCエンドポイントを使用して、プライベートサブネット内のEC2インスタンスからAmazon S3リソースへ安全にアクセスする方法を学びます。インターネット経由のアクセスを排除し、S3バージョニングでデータ保護を強化します。
tag: Amazon VPC, Amazon S3, Amazon EC2, AWS Systems Manager (Session Manager)



[**Working with Amazon VPC Network Access Analyzer (日本語)**](https://explore.skillbuilder.aws/learn/courses/16360/working-with-amazon-vpc-network-access-analyzer-ri-ben-yu)
Amazon VPC Network Access Analyzerを使って、AWSネットワークのセキュリティ状態を評価・検証し、コンプライアンス要件に合致していることを実証します。インターネットゲートウェイからの受信トラフィック、VPCエンドポイントパス、プライベートサブネットのインターネットアクセス、VPCセグメンテーションなど、様々なネットワーク構成を分析します。
tag: Amazon VPC(サブネット、ルートテーブル、ネットワークACL、セキュリティグループ、インターネットゲートウェイ、NATゲートウェイ、VPCピアリング接続、VPCエンドポイント), Amazon VPC Network Access Analyzer



[**Building with Amazon DynamoDB Tables (日本語)**](https://explore.skillbuilder.aws/learn/courses/16717/building-with-amazon-dynamodb-tables-ri-ben-yu)
Amazon DynamoDBへのJSONデータのインポート、複雑なクエリの実行、**DynamoDB Accelerator (DAX)**によるパフォーマンス向上を学びます。さらに、DynamoDBのバックアップ、復元、モニタリングオプションも探究します。
tag: Amazon DynamoDB, Amazon DynamoDB Accelerator (DAX), Amazon EC2, Amazon CloudWatch, Amazon SNS


[**Caching Static Files with Amazon CloudFront (日本語)**](https://explore.skillbuilder.aws/learn/courses/7752/caching-static-files-with-amazon-cloudfront-ri-ben-yu)
Amazon S3にホストされた静的ウェブサイトをAmazon CloudFrontで配信し、コンテンツ配信を高速化します。CloudFrontディストリビューションの作成、設定、コンテンツの更新・無効化を学び、世界中のエッジロケーションからコンテンツを効率的に提供する方法を理解します。
tag: Amazon CloudFront, Amazon S3


[**Auditing Your Security with AWS Trusted Advisor (日本語)**](https://explore.skillbuilder.aws/learn/courses/6930/auditing-your-security-with-aws-trusted-advisor-ri-ben-yu)
AWS Trusted Advisorを用いてAWSリソースのセキュリティ監査を行い、基本的なセキュリティベストプラクティスへの準拠を確認します。具体的には、Amazon EC2セキュリティグループの不適切なポート設定の修正、多要素認証（MFA）の設定、およびAWS IAMの操作方法を学びます。
tag: AWS Trusted Advisor, Amazon EC2, AWS IAM


[**Configuring and Deploying Amazon VPC for a 3-tier Web App (日本語)**](https://explore.skillbuilder.aws/learn/courses/6951/configuring-and-deploying-amazon-vpc-for-a-3-tier-web-app-ri-ben-yu)
AWSクラウド上に3層ウェブアプリケーションをサポートするAmazon VPCインフラストラクチャを構築・デプロイします。VPC、パブリック/プライベートサブネット、インターネットゲートウェイ、NATゲートウェイ、ルートテーブル、セキュリティグループを設定し、Amazon RDSとAmazon EC2インスタンスにアプリケーションをデプロイ後、Application Load Balancerで公開します。
tag: Amazon VPC, Amazon EC2, Amazon RDS, Elastic Load Balancing (Application Load Balancer)


[**Building with Amazon DocumentDB Databases (日本語)**](https://explore.skillbuilder.aws/learn/courses/18818/building-with-amazon-documentdb-databases-ri-ben-yu)
リレーショナルデータを非リレーショナルデータモデルに変換し、変換後のデータをAmazon DocumentDBにインポートする方法を学びます。データのロード、クエリの実行、バックアップ、パフォーマンスモニタリング、フェイルオーバーのシミュレーションを通じてDocumentDBの運用を体験します。
tag: Amazon DocumentDB, Amazon EC2, Amazon API Gateway, AWS Lambda, AWS Secrets Manager
Amazon CloudWatch



[**Filtering and blocking web incursions with AWS WAF (日本語)**](https://explore.skillbuilder.aws/learn/courses/13341/filtering-and-blocking-web-incursions-with-aws-waf-ri-ben-yu)
AWS WAFを使ってウェブアプリケーションへのSQLインジェクション（SQLi）やクロスサイトスクリプティング（XSS）攻撃を防ぎます。まず、OWASP ZAPを用いてこれらの脆弱性を特定し、次にAWS WAFでウェブACLを作成し、AWSマネージドルールグループとカスタムルールを適用してアプリケーションを保護します。
tag: AWS WAF (Web Application Firewall), Amazon CloudFront, AWS Systems Manager (Fleet Manager)


[**Zero Trust Architecture for Service-To-Service Workloads (日本語)**](https://explore.skillbuilder.aws/learn/courses/16251/zero-trust-architecture-for-service-to-service-workloads-ri-ben-yu)
サービス間ワークロードにゼロトラストアーキテクチャを実装し、Amazon API Gateway、AWS Identity and Access Management (IAM)、Amazon Virtual Private Cloud (VPC)、VPCエンドポイントのセキュリティグループルールを強化することで、セキュリティ体制を改善します。これにより、従来のネットワーク中心の制御から、アイデンティティとネットワークの両方を組み合わせた多層的なセキュリティモデルへ移行します。
tag: Amazon API Gateway, AWS IAM, Amazon VPC, Amazon EC2, AWS Lambda


[**Troubleshooting Website Reachability behind a Load Balancer (日本語)**](https://explore.skillbuilder.aws/learn/courses/21480/troubleshooting-website-reachability-behind-a-load-balancer-ri-ben-yu)
Elastic Load Balancing (ELB) の背後にあるウェブサイトにユーザーがアクセスできないシナリオをトラブルシューティングします。Application Load Balancer (ALB)、Amazon EC2インスタンス、関連するネットワーク設定を確認・修正し、ウェブサイトへのアクセスと高可用性を実現します。
tag: Elastic Load Balancing (ELB), Application Load Balancer (ALB), Amazon EC2, Amazon VPC


[**Collecting and Analyzing Logs with Amazon CloudWatch Logs Insights (日本語)**](https://explore.skillbuilder.aws/learn/courses/6943/collecting-and-analyzing-logs-with-amazon-cloudwatch-logs-insights-ri-ben-yu)
N層ウェブアプリケーションのログを収集・分析し、セキュリティ脆弱性を調査します。AWS Systems ManagerでAmazon EC2にCloudWatch エージェントをインストールし、ウェブサーバー、システム、Amazon VPC フローログ、Amazon RDSデータベースログをAmazon CloudWatch Logsに集約し、CloudWatch Logs Insightsで分析します。
tag: Amazon CloudWatch Logs, Amazon CloudWatch Logs Insights, AWS Systems Manager, Amazon EC2, Amazon VPC, Amazon RDS


[**Event Driven Architecture with Amazon API Gateway, Amazon EventBridge and AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/15560/event-driven-architecture-with-amazon-api-gateway-amazon-eventbridge-and-aws-lambda-ri-ben-yu)
Amazon API Gateway、Amazon EventBridge、AWS Lambdaを組み合わせて、イベント駆動型のサーバーレスアーキテクチャを構築します。HTTP APIでリクエストを受け取りEventBridgeへ連携、EventBridgeのルールでLambda関数を呼び出し、処理されたイベントをWebSocket経由でクライアントへリアルタイムに通知します。
tag: Amazon API Gateway, Amazon EventBridge, AWS Lambda


[**Refactoring Legacy Apps to Microservices using AWS Migration Hub Refactor Spaces (日本語)**](https://explore.skillbuilder.aws/learn/courses/21747/refactoring-legacy-apps-to-microservices-using-aws-migration-hub-refactor-spaces-ri-ben-yu)
AWS Migration Hub Refactor Spacesを使用して既存のモノリシックアプリケーションをマイクロサービスアーキテクチャにリファクタリングするプロセスを段階的に学びます。ショッピングカート機能をAWS LambdaとAmazon DynamoDBで構築された新しいマイクロサービスへ移行し、トラフィックルーティングを定義することで、レガシーシステムと新サービスを並行稼働させます。
tag: AWS Migration Hub Refactor Spaces, AWS Lambda, Amazon DynamoDB, Amazon S3, Amazon API Gateway


[**Working with Amazon CloudFront for Dynamic Content Acceleration (日本語)**](https://explore.skillbuilder.aws/learn/courses/7750/working-with-amazon-cloudfront-for-dynamic-content-acceleration-ri-ben-yu)
Amazon CloudFront を使用して動的なウェブサイト（phpBBフォーラム）のコンテンツ配信を高速化します。Amazon EC2上で動作する動的サイトと静的コンテンツの両方をCloudFrontのグローバルエッジネットワークを介して配信・最適化し、ユーザーエクスペリエンスを向上させます。
tag: Amazon CloudFront, Amazon EC2, Amazon S3


[**Lab - Monitoring Micro-Service Architectures with AWS X-Ray and Amazon CloudWatch (日本語)**](https://explore.skillbuilder.aws/learn/courses/21975/lab-monitoring-micro-service-architectures-with-aws-x-ray-and-amazon-cloudwatch-ri-ben-yu)
マイクロサービスアーキテクチャの監視にAWS X-RayとAmazon CloudWatchを活用する方法を学びます。X-Rayの設定を有効化し、サービスマップの作成、エンドツーエンドのリクエストの可視化、トレースデータの確認を行います。
tag: AWS X-Ray, Amazon CloudWatch, Amazon EC2


[**Building with Amazon Redshift Clusters (日本語)**](https://explore.skillbuilder.aws/learn/courses/17376/building-with-amazon-redshift-clusters-ri-ben-yu)
Amazon Redshiftクラスターを構築し、SQL Workbenchを使用してIMDbデータセットを効率的に分析する方法を学びます。データのインポート（COPYコマンド、マニフェストファイル）、エクスポート（UNLOADコマンド）、パフォーマンス最適化のためのVACUUM/ANALYZEコマンド、そしてSORTKEYとDISTKEYの使用方法について習得します。
tag: Amazon Redshift, Amazon S3


[**Build a Serverless Text-to-Speech Application with Amazon Polly (日本語)**](https://explore.skillbuilder.aws/learn/courses/11628/build-a-serverless-text-to-speech-application-with-amazon-polly-ri-ben-yu)
Amazon Pollyを活用してサーバーレスなテキスト読み上げアプリケーションを構築します。テキストから音声を生成し、Amazon S3に保存されたウェブUIを介して、Amazon API Gateway、AWS Lambda、Amazon SNS、Amazon DynamoDBを連携させ、リアルタイムかつ効率的な音声合成サービスを提供します。
tag: Amazon Polly, AWS Lambda, Amazon API Gateway, Amazon S3, Amazon DynamoDB, Amazon SNS




[****]()
[****]()


[**Serverless Architectures with Amazon DynamoDB and Amazon Kinesis Streams with AWS Lambda (日本語)**](https://explore.skillbuilder.aws/learn/courses/7754/serverless-architectures-with-amazon-dynamodb-and-amazon-kinesis-streams-with-aws-lambda-ri-ben-yu)
アクセス権がないようです

[**Migrate a Monolith Web Application to AWS Using Application Migration Service (日本語)**](https://explore.skillbuilder.aws/learn/courses/15759/migrate-a-monolith-web-application-to-aws-using-application-migration-service-ri-ben-yu)
アクセス権がないようです

[**Migrating Web Application to Cloud using AWS Elastic Beanstalk (日本語)**](https://explore.skillbuilder.aws/learn/courses/14421/migrating-web-application-to-cloud-using-aws-elastic-beanstalk-ri-ben-yu)
アクセス権がないようです


[**Stock Replenishment App (日本語)**](https://explore.skillbuilder.aws/learn/courses/17671/stock-replenishment-app-ri-ben-yu)
アクセス権がないようです


[**Managing Access at Scale with Amazon S3 Access Points (日本語)**](https://explore.skillbuilder.aws/learn/courses/21829/managing-access-at-scale-with-amazon-s3-access-points-ri-ben-yu)
アクセス権がないようです


[**Controlling the Network (日本語)**](https://explore.skillbuilder.aws/learn/courses/13887/controlling-the-network-ri-ben-yu)
問い合わせ中
途中

[**Building and Deploying a Containerized Application with Amazon Elastic Kubernetes Service (日本語)**](https://explore.skillbuilder.aws/learn/courses/15348/building-and-deploying-a-containerized-application-with-amazon-elastic-kubernetes-service-ri-ben-yu)
[**Create a CI/CD pipeline to deploy your app to AWS Fargate (日本語)**](https://explore.skillbuilder.aws/learn/courses/15314/create-a-cicd-pipeline-to-deploy-your-app-to-aws-fargate-ri-ben-yu)
アクセス権がない

[**Secure Your Account During an Active Event (日本語)**](https://explore.skillbuilder.aws/learn/courses/15851/secure-your-account-during-an-active-event-ri-ben-yu)
ラボは現在メンテナンス中です。後でもう一度試すか、別のラボを選択してください。


Building with Amazon RDS Databases
Media Services: Use AWS AI services to automate captioning & subtitling
Comparing Amazon Virtual Private Cloud(VPC) peering and AWS Transit Gateway
Streaming Dynamic Content using Amazon CloudFront Troubleshooting Network Connectivity in a Peered VPC
Scale Your Security Vulnerability Testing with Amazon Inspector

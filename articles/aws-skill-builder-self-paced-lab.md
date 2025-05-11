---
title: "aws skill builder self paced lab"
emoji: "👻"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["aws"]
published: false
---

インスタンスクラス
IAM拒否
db.t3.medium

RDPのURLでアクセスできない
Systems Manager → フリートマネージャー → リモートデスクトップ
![](https://storage.googleapis.com/zenn-user-upload/d9602df03776-20250501.png =600x)


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



[****]()
[****]()


EMR File System Client-side Encryption Using AWS KMS-managed Keys
Building and Deploying a Containerized Application with Amazon Elastic Kubernetes
Create a CI/CD pipiline to deploy your app to AWS Fargate
Maintaining High Availability with Auto Scaling
Building Highly Available Web Application
Lab - Build a Product Recommendation Engine using Amazon Neptune
Migratino RDS MySQL to Aurora with Read Replica
Effortless Relational Scalability with Amazon Aurora Serverless v2
Amazon DynamoDB CRUD Activities Using the AWS CLI and SDK
Amazon DynamoDB Capacity Sizing
Amazon DynamoDB - Monitoring
Amazon DynamoDB Scans, Queries, and Indexes
Amazon DynamoDB Streams and TTL
Building with Amazon Aurora Databases
Building with Amazon DocumentDB Databases
Building with Amazon Redshift Clusters
Building with Amazon RDS Databases
Building with Amazon DynamoDB Tables
Automating AWS Services with Scripting and the AWS CLI
.NET Workloads on AWS Lambda
Stock Replenishment App
AWS Federated Authentication with AD FS
Collecting and Analyzing Logs with Amazon CloudWatch Logs Insights
Lauching and Managing a Web Application with AWS CloudFormation
Lab - Monitoring Micro-Service Architectures with AWS X-Ray and Amazon CloudWatch
Media Services: Use AWS AI services to automate captioning & subtitling
Migrating Web Application to Cloud using AWS Elastic Beastalk
Migrate a Monolith Web Application to AWS Using Application Migration Service
Refactoring Legacy Apps to Microservices using AWS Migration Hub Refactor Spaces
AWS Network Firewall Fundamentals
Configuring and Deploying Amazon VPC for a 3-tier Web App
Caching Static Files with Amazon CloudFront
Comparing Amazon Virtual Private Cloud(VPC) peering and AWS Transit Gateway
Streaming Dynamic Content using Amazon CloudFront Troubleshooting Network Connectivity in a Peered VPC
Troubleshooting Website Reachability behind a Load Balancer
Working with Amazon VPC Network Access Analyzer
Working with Amazon CloudFront for Dynamic Content Acceleration
Auditing Your Security with AWS Trusted Advisor
Filtering and blocking web incursions with AWS WAF
My Bucket, My Rules
Securing the Endpoing
Controlling the Network
Scale Your Security Vulnerability Testing with Amazon Inspector
Lab - Troubleshooting - IAM Access Issues
Secure Your Account During an Active Event
Zero Trust Architecture for Service-To-Service Workloads
Managing Access at Scale with Amazon S3 Access Points
Managing Access to Amazon S3 Resources with Amazon VPC Endpoints
Serverless Architectures with Amazon DynamoDB and Amazon Kinesis Streams with AWS
Event Driven Architecture with Amazon API Gateway, Amazon EventBridge and AWS Lambda
Build a Serverless Text-to-Speech Application with Amazon Polly
Update Security Groups Automatically Using AWS Lambda
Troubleshooting API Gateway with Lambda Proxy Integration

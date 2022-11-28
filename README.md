# A tour of AWS ☄️

這份文件主要會記錄我個人學習 AWS 雲端架構的學習筆記， 本文件的內容會涵蓋 AWS Solution Architect Associate（SAA）的考試範圍。
同時這份文件也會整理一些我個人覺得還不錯的技術文件並且適時地補充與 AWS 有關的核心概念以及一些不錯的實戰範例（以網路上普遍認可的 Best Pratice 為主）。

## AWS 簡介

參考 AWS 的官方文件或是網路上其他人的考試心得，不難發現 AWS 有幾項核心功能：
- Computing
- Networking
- Security
- Storage
- Authentication & Authorization 
- High-scalable service
- Infrastructure

### Computing

包含 EC2（VM）、EKS（Kubernetes）、ECS（Docker）、ECR（Container Registry）。

### Networking

包含 VPC（虛擬網路）、VPN（包含 Client VPN 和 Site-to-Site VPN）以及相關的虛擬資源（NAT Gateway、Internet Gateway、Router53）。

### Security

Security 會涉及到的層面更廣，下至惡意流量偵測、黑名單白名單，上至系統設計（System Design）、公有雲的帳戶權限管理（IAM）。

### Storage

AWS 提供各式各樣的儲存服務：
- [EBS](https://aws.amazon.com/tw/ebs/)（與 AWS EC2 配合使用的高效能儲存空間）
- S3（可經由 REST、SOAP 或是 BitTorrent 將靜態檔案上傳至網路空間中）
  [AWS S3](https://aws.amazon.com/tw/s3/) 又可依據 Availability 與 Cost 細分成 S3、S3-IA、Glacier。
- [AWS RDS](https://aws.amazon.com/tw/rds/)（關聯式資料庫）
- [AWS DynamoDB](https://aws.amazon.com/tw/dynamodb/)（非關聯式資料庫）

### Authentication & Authorization

AWS 提供 Role 以及 Policy（[IAM](https://docs.aws.amazon.com/zh_tw/IAM/latest/UserGuide/introduction.html)）讓公有雲帳號的管理者可以為個人組織拆分部門，並且個別賦予這些部門所需要的存取權限。
比如說：DevOps Team 需要有 Cloud Formation 服務的存取權限。


### High-scalable service

了解 AWS 的基礎元件後，最重要的事情便是設計一套高可用性、可靠的網路服務，核心會包含 [Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-groups.html)、[CloudWatch](https://aws.amazon.com/tw/cloudwatch/)、[CloudFormation](https://aws.amazon.com/tw/cloudformation/) 這幾項技術的相互配合。

### Infrastructure

包含 IaC（Infrastructure as Code）、CloudFormation、[AWS Lambda](https://aws.amazon.com/tw/lambda/) 等技術。


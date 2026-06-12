# Day 3: VPC・ネットワーク設計

**学習日：2026-06-12**
**学習時間：3時間**
**習得度：96%**

## 🎯 学習内容

### セクション 1: VPC・サブネット・CIDR（45分）
- CIDR 表記法を理解
- サブネット計算（/24 = 256個のIP、AWS が予約する5個を差し引いて251個）
- マルチAZ 設計パターンを習得

### セクション 2: ルーティング・ゲートウェイ（45分）
- Internet Gateway（IGW）の役割
- NAT Gateway で Private Subnet から外部通信
- ルートテーブルの設定（0.0.0.0/0 → IGW）

### セクション 3: セキュリティグループ・NACL（45分）
- セキュリティグループ：ステートフル（リソース単位）
- NACL：ステートレス（サブネット単位）
- 実務的なルール設計パターン

### セクション 4: VPC 実装ハンズオン（45分）
- AWS CLI で VPC・サブネット・IGW・ルートテーブル を作成
- マルチAZ（AZ-a, AZ-c）VPC 構築完了
- 全リソースが正常に構築され、接続確認完了

## 📦 構築したリソース

**VPC: vpc-0aef2161c7d9c78ad (10.0.0.0/16)**

### Public Subnets（インターネット接続）
- Public Subnet 1（AZ-a）: 10.0.1.0/24
- Public Subnet 2（AZ-c）: 10.0.2.0/24

### Private Subnets（VPC 内通信のみ）
- Private Subnet 1（AZ-a）: 10.0.10.0/24
- Private Subnet 2（AZ-c）: 10.0.11.0/24

### ネットワークリソース
- Internet Gateway: igw-0242e34998bdefb2b
- Public Route Table: rtb-003f7731938c813c4（IGW へのルート追加済み）
- Private Route Table: rtb-0ef50015b78a1e2ed（VPC 内通信のみ）

## ✅ 習得したスキル

- ✅ CIDR 計算ができる
- ✅ VPC・サブネット設計ができる
- ✅ ルーティング・ゲートウェイを理解できる
- ✅ セキュリティグループ・NACL を設計できる
- ✅ AWS CLI で VPC を構築できる
- ✅ マルチAZ ネットワーク設計ができる

## 📊 Day 2-3 習得度の推移
---

**Day 3 完了！** 🎉

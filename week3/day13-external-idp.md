# Day 13: 外部Identity Provider連携 完全習得

**実施日**: 2026-06-19
**習得度**: 85%
**方針**: 概念学習ベース（ハンズオンなし・コスト発生ゼロ）

## Section 1: SAML2.0・外部IdP 詳細
- SP = AWS IAM Identity Center（サービス提供側）
- IdP = Azure Entra ID（認証側）
- SAML2.0 7ステップ（SP-Initiated）
- SAML Assertion 4要素：Subject・Conditions・Attributes・Signature


## Section 2: メタデータ設定・属性マッピング
- SP メタデータ：Entity ID・ACS URL・公開鍵証明書
- IdP メタデータ：Entity ID・SSO URL・公開鍵証明書
- Name ID = メールアドレスでユーザーを一意識別
- SCIM + 属性マッピング併用が案件①推奨構成

## Section 3: SSOログインテスト概念
- ログイン成功確認5項目
- AWS内部4検証（署名・有効期限・Audience・Assignment）
- CLI SSO設定（~/.aws/config）・aws sso login

## Section 4: トラブルシューティング概念
- エラー①署名検証エラー → IdPメタデータ再登録
- エラー②Assignmentなし → Assignment追加
- エラー③属性マッピング不一致 → マッピング設定修正
- エラー④SCIMトークン期限切れ → トークン再発行
- エラー⑤セッション切れ → SSO Portalから再ログイン
- CloudTrail：AssumeRoleWithSAML イベントで調査

## 課金リソース：ゼロ ✅

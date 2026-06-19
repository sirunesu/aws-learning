# Day 15: AWS Config・CloudTrail・監査ログ統合

## Config の4コンポーネント
- Recorder：設定変更をリアルタイム記録
- Rules：準拠・違反を評価
- Conformance Pack：複数 Rules のテンプレート
- Remediation：SSM Automation で自動修復

## CloudTrail vs Config
- CloudTrail：誰が・いつ・何の操作をしたか（API ログ）
- Config：設定がどう変化したか（スナップショット）
- 組み合わせで完全追跡が可能

## Aggregator
- 複数 Account・Region の Config データを Audit Account に集約
- AllAwsAccounts=true / AllAwsRegions=true

## Remediation 安全設計
- MaximumAutomaticAttempts: 5（無限ループ防止）
- RetryAttemptSeconds: 60（60秒待って再試行）

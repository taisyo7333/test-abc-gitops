# test-abc-gitops

このリポジトリは 1 回の払い出し専用です。共有の platform-gitops には置きません。

- `config.json` は同期先 Namespace とアプリ名。ApplicationSet が読む。`apiVersion` は無い
- Namespace `test`
- Deployment `test-abc` replicas 2
- ServiceAccount の `eks.amazonaws.com/role-arn` は `arn:aws:iam::977099000999:role/s3read-test-test-abc`
- Pipeline が CloudFormation でバケット `test-abc-dinoue` と IAM ロールを作り、イメージをビルドします

# モノレポ: pnpm + Turborepo

pnpm を使う。pnpm workspace によるモノレポ管理が目的。
Turborepo でタスクの依存関係解決とキャッシュを行う。

## workspace 構造

```yaml
packages:
  - "packages/*"
  - "apps/*"
  - "configs/*"
  - "infra"
```

| ディレクトリ | 置くもの |
|---|---|
| `packages/` | 共有ライブラリ。ドメインロジック、UI コンポーネント、ユーティリティなど、複数の app から使われるコード。 |
| `apps/` | デプロイ単位のアプリケーション。Web フロントエンド、API サーバーなど。 |
| `configs/` | 共有設定。ESLint、TypeScript などの設定パッケージ。各パッケージから extend して使う。 |
| `infra` | AWS CDK によるインフラ定義。アプリケーションコードとは独立してデプロイする。 |

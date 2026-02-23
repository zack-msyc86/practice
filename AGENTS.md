# Coding Knowledge Base

人と AI の両方が参照できるコーディング知見集。
CLAUDE.md として配置すれば、Claude Code が自動的に読み込む。

## メタ学習ルール

コーディング規約や運用ルールについて指摘を受けたら：

1. 根本原因を分析する
2. 同じ問題を防ぐためのルールを適切なカテゴリに追加する
3. 追加したルールを明示的に説明する

これにより、同じ指摘を繰り返さず、知識が蓄積される。

## ドキュメント記述ルール

- コードから自明なことは書かない
- タイトルと無関係な情報を含めない
- 他で説明済みの内容を重複して書かない（公式ドキュメント等）
- **「結果」ではなく「意図」を書く** — なぜそうしたのかという設計判断の理由だけを書く
- **ドキュメントのスコープを守る** — そのドキュメントのテーマに集中する
- 不要なコード例は載せず、要点だけ簡潔に書く

## カテゴリ

### coding-style/
- [declarative.md](coding-style/declarative.md) — 宣言的・関数型スタイル
- [result-type.md](coding-style/result-type.md) — バックエンド・コアロジックで Result 型を使う

### react/
- [use-fc.md](react/use-fc.md) — FC 型でコンポーネントを定義
- [single-component-per-file.md](react/single-component-per-file.md) — 1 ファイル 1 コンポーネント
- [avoid-use-effect.md](react/avoid-use-effect.md) — useEffect の使用を避ける

### typescript/
- [esm-only.md](typescript/esm-only.md) — ESM のみ、CJS を避ける
- [naming-convention.md](typescript/naming-convention.md) — 命名規則（kebab / PascalCase / snake_case / SCREAMING_SNAKE_CASE）
- [no-any-type.md](typescript/no-any-type.md) — `any` 型の使用禁止

### frontend/
- [nextjs.md](frontend/nextjs.md) — Next.js（Server Components が前提）

### backend/
- [hono.md](backend/hono.md) — API フレームワークは Hono

### data-fetching/
- [colocation.md](data-fetching/colocation.md) — コンポーネントによるデータのコロケーション

### graphql/
- [code-first.md](graphql/code-first.md) — コードファースト（スキーマファーストの型問題を回避）

### database/
- [drizzle-orm.md](database/drizzle-orm.md) — ORM は Drizzle ORM
- [schema-pattern.md](database/schema-pattern.md) — テーブル分解パターン

### design-styling/
- [css-and-vanilla-extract.md](design-styling/css-and-vanilla-extract.md) — CSS + Vanilla Extract

### linting/
- [eslint-only.md](linting/eslint-only.md) — ESLint のみ、Prettier なし
- [praha-eslint-config.md](linting/praha-eslint-config.md) — @praha/eslint-config を使用

### testing/
- [data-setup.md](testing/data-setup.md) — beforeEach でデータ準備、test は assert のみ

### monorepo/
- [pnpm-and-turbo.md](monorepo/pnpm-and-turbo.md) — pnpm workspace + Turborepo
- [turbo-tasks.md](monorepo/turbo-tasks.md) — generate / build / dev のタスク設計

### devops/
- [renovate.md](devops/renovate.md) — Mend Renovate で依存関係を自動更新
- [release-strategy.md](devops/release-strategy.md) — trunk-based + Feature Flag

### libraries/
- [storybook/playwright-verification.md](libraries/storybook/playwright-verification.md) — Storybook + Playwright による動作確認
- [storybook/play-function.md](libraries/storybook/play-function.md) — play 関数のクエリ
- [storybook/snapshot-stories.md](libraries/storybook/snapshot-stories.md) — スナップショット向け Story 設計
- [vanilla-extract/use-style-variants.md](libraries/vanilla-extract/use-style-variants.md) — styleVariants を使う
- [pothos/file-layout.md](libraries/pothos/file-layout.md) — ファイル構成パターン
- [conform/future-api.md](libraries/conform/future-api.md) — Future API の使い方


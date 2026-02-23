# zack-msyc86/practice

zack-msyc86 個人のコーディング知見集。
プロジェクトで [vivify](https://github.com/zack-msyc86/vivify) により蓄積した知見のうち、汎用的なものをここに昇格させる。

## 使い方

- **個人**: `~/.claude/CLAUDE.md` にこのリポジトリのパスを書いておけば、全プロジェクトで自動的にコンテキストに載る。
- **チーム**: git submodule としてプロジェクトに取り込み、`CLAUDE.md` から参照する。

## ドキュメント一覧

### coding-style/
- [declarative.md](coding-style/declarative.md) — 宣言的・関数型スタイル
- [result-type.md](coding-style/result-type.md) — Result 型

### react/
- [use-fc.md](react/use-fc.md) — Use FC
- [single-component-per-file.md](react/single-component-per-file.md) — Single Component Per File
- [avoid-use-effect.md](react/avoid-use-effect.md) — useEffect の使用を避ける
- [no-generics.md](react/no-generics.md) — コンポーネントにジェネリクスを使わない

### typescript/
- [esm-only.md](typescript/esm-only.md) — ESM のみ
- [naming-convention.md](typescript/naming-convention.md) — 命名規則
- [no-any-type.md](typescript/no-any-type.md) — `any` 型の使用禁止

### frontend/
- [nextjs.md](frontend/nextjs.md) — フロントエンド: Next.js

### backend/
- [hono.md](backend/hono.md) — API フレームワーク: Hono

### data-fetching/
- [colocation.md](data-fetching/colocation.md) — コンポーネントによるデータのコロケーション

### graphql/
- [code-first.md](graphql/code-first.md) — GraphQL: コードファースト

### database/
- [drizzle-orm.md](database/drizzle-orm.md) — ORM: Drizzle ORM
- [schema-pattern.md](database/schema-pattern.md) — Database Schema Pattern

### design-styling/
- [css-and-vanilla-extract.md](design-styling/css-and-vanilla-extract.md) — スタイリング: CSS + Vanilla Extract

### linting/
- [eslint-only.md](linting/eslint-only.md) — ESLint のみ（Prettier なし）
- [praha-eslint-config.md](linting/praha-eslint-config.md) — @praha/eslint-config

### testing/
- [data-setup.md](testing/data-setup.md) — テストのデータ準備

### monorepo/
- [pnpm-and-turbo.md](monorepo/pnpm-and-turbo.md) — モノレポ: pnpm + Turborepo
- [turbo-tasks.md](monorepo/turbo-tasks.md) — Turborepo のタスク設計

### devops/
- [renovate.md](devops/renovate.md) — 依存関係の更新: Mend Renovate
- [release-strategy.md](devops/release-strategy.md) — リリース戦略
- [continuous-rotation.md](devops/continuous-rotation.md) — 常に回し続ける

### libraries/
- [storybook/playwright-verification.md](libraries/storybook/playwright-verification.md) — Storybook + Playwright による動作確認
- [storybook/play-function.md](libraries/storybook/play-function.md) — Storybook play 関数のクエリ
- [storybook/snapshot-stories.md](libraries/storybook/snapshot-stories.md) — Storybook スナップショット向け Story 設計
- [vanilla-extract/use-style-variants.md](libraries/vanilla-extract/use-style-variants.md) — Use styleVariants
- [pothos/file-layout.md](libraries/pothos/file-layout.md) — Pothos File Layout
- [conform/future-api.md](libraries/conform/future-api.md) — Conform Future API

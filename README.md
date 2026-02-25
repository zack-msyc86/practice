# zack-msyc86/practice

個人のコーディング知見集。[vivify](https://github.com/zack-msyc86/vivify) で蓄積した知見のうち汎用的なものを昇格。

## 使い方

- **個人**: `~/.claude/CLAUDE.md` に `@path/to/practice/README.md` を書けば全プロジェクトで自動参照
- **チーム**: git submodule で取り込み `CLAUDE.md` に `@practice/README.md` で参照

## 一覧

### coding-style/
- [result-type.md](coding-style/result-type.md) — バックエンドでは Result 型 (byethrow) を使う

### react/
- [use-fc.md](react/use-fc.md) — FC + ComponentPropsWithRef でコンポーネント定義
- [single-component-per-file.md](react/single-component-per-file.md) — 1 ファイル 1 コンポーネント + .css.ts + index.ts
- [avoid-use-effect.md](react/avoid-use-effect.md) — useEffect は外部システム同期のみ
- [no-generics.md](react/no-generics.md) — コンポーネントにジェネリクスを使わない

### frontend/
- [nextjs.md](frontend/nextjs.md) — Next.js（Server Components でデータコロケーション）

### backend/
- [hono.md](backend/hono.md) — API は Hono（Web Standard API）

### data-fetching/
- [colocation.md](data-fetching/colocation.md) — GraphQL か Server Component でデータ取得。コンポーネントとデータ要求を同じ場所に

### graphql/
- [code-first.md](graphql/code-first.md) — コードファースト（Pothos）。parent の型安全のため

### database/
- [drizzle-orm.md](database/drizzle-orm.md) — ORM は Drizzle（SQL をほぼそのまま書ける）
- [schema-pattern.md](database/schema-pattern.md) — Nullable カラムより別テーブル分割。UPDATE 最小化

### design-styling/
- [css-and-vanilla-extract.md](design-styling/css-and-vanilla-extract.md) — CSS + Vanilla Extract（CSS の知識がそのまま使える）

### linting/
- [eslint-only.md](linting/eslint-only.md) — ESLint のみ（Prettier なし）。@praha/eslint-config 使用

### testing/
- [data-setup.md](testing/data-setup.md) — beforeEach でデータ準備、test では assert のみ

### monorepo/
- [pnpm-and-turbo.md](monorepo/pnpm-and-turbo.md) — pnpm workspace + Turborepo
- [turbo-tasks.md](monorepo/turbo-tasks.md) — generate → build → dev の 3 タスク設計

### devops/
- [release-strategy.md](devops/release-strategy.md) — staging=main 追従、production=GitHub Release + Feature Flag
- [continuous-rotation.md](devops/continuous-rotation.md) — デプロイ・シークレットのローテーションを常に回す

### libraries/
- [storybook/playwright-verification.md](libraries/storybook/playwright-verification.md) — Storybook + playwright-cli で動作確認
- [storybook/play-function.md](libraries/storybook/play-function.md) — play 関数では findByRole（getByRole は NG）
- [storybook/snapshot-stories.md](libraries/storybook/snapshot-stories.md) — 1 Story = 1 視覚状態。setTimeout 禁止
- [vanilla-extract/use-style-variants.md](libraries/vanilla-extract/use-style-variants.md) — styleVariants を使う（recipe は使わない）
- [pothos/file-layout.md](libraries/pothos/file-layout.md) — __type.ts + 個別フィールド + index.ts
- [conform/future-api.md](libraries/conform/future-api.md) — @conform-to/*/future API の使い方

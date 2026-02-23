# Coding Knowledge Base

コーディングの知見を蓄積・共有するためのリポジトリ。
人にも AI にも読みやすい構造で管理する。

## 使い方

### AI エージェントに読ませる

`CLAUDE.md`（`AGENTS.md` へのシンボリックリンク）をプロジェクトルートに置くと、Claude Code が自動的に読み込む。

このリポジトリの知見を別プロジェクトで使うには：
1. このリポジトリを submodule やコピーとして取り込む
2. `AGENTS.md` の必要な部分をプロジェクトの `CLAUDE.md` に組み込む

### 人が読む

カテゴリ別のディレクトリを辿って、関連する知見を参照する。

## 構造

```
├── AGENTS.md          # AI 向けインデックス（CLAUDE.md のリンク元）
├── coding-style/      # コーディングスタイル（宣言的、Result 型）
├── react/             # React の規約
├── typescript/        # TypeScript の規約
├── frontend/          # フロントエンド技術選定
├── backend/           # バックエンド技術選定
├── data-fetching/     # データ取得アーキテクチャ
├── graphql/           # GraphQL の設計方針
├── database/          # DB 設計 + 技術選定
├── design-styling/    # スタイリング技術選定
├── linting/           # リンター・フォーマッター
├── testing/           # テストの書き方
├── devops/            # CI/CD・リリース戦略
└── libraries/         # ライブラリ固有の使い方
    ├── storybook/
    ├── vanilla-extract/
    ├── pothos/
    └── conform/
```

## ドキュメントの種類

- **技術選定** — 何を使うか、なぜ使うか（各テーマディレクトリ内）
- **コーディング規約** — どう書くか（各テーマディレクトリ内）
- **ライブラリの使い方** — 特定ライブラリの API パターンやベストプラクティス（`libraries/` 内）

# Pothos File Layout

schema.graphql の構造と対応させる。

## ディレクトリ構造

トップレベルに型（Query, Mutation, User 等）がディレクトリとして並ぶ。

```
presentation/
├── query/
│   ├── __type.ts
│   ├── users.ts
│   └── index.ts
├── user/
│   ├── __type.ts
│   ├── posts.ts
│   └── index.ts
```

## ファイルの分離基準

- **`__type.ts`** — 型自身が直接提供するもの（ParentType の定義 + `t.expose*` フィールド）
- **個別ファイル** — 型の外から取得するもの（カスタム resolver が必要なフィールド）
- **`index.ts`** — 全ファイルを re-export して登録

`t.expose*` は ParentType のプロパティをそのまま公開するだけなので、ParentType の定義と本質的に同じ関心。

## 値オブジェクト

ID を持たない値オブジェクトも同様に、独自ディレクトリの `__type.ts` で `objectRef` + `implement` で定義する。

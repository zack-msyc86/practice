# Use FC

- `FC` 型でコンポーネントを定義
- props は `ComponentPropsWithRef<'要素'>` をベースに拡張
- コンポーネント固有の props のみ型定義に追加（`children` は `FC` が提供）

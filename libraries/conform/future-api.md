# Conform Future API

`@conform-to/react/future` / `@conform-to/valibot/future` を使用。

## スキーマ

- `coerceFormValue` で必ずラップする（空文字列 → `undefined` 変換、配列の自動変換）
- 型付き定数がある場合は `picklist` を使う

```ts
import { coerceFormValue } from '@conform-to/valibot/future';

export const schema = coerceFormValue(
  object({ ... }),
);
```

## フォーム (Client)

- `useForm(schema, options)` のスキーマファースト形式
- `shouldValidate` / `shouldRevalidate` は Provider で一括設定可能。個別指定が不要になる
- フィールドに `aria-invalid` / `aria-describedby`、エラー要素に `id={field.errorId}` を付与
- クロスフィールドバリデーションは `onValidate` の `schemaValue` を使う

## サーバーアクション

- `parseSubmission` → `safeParse` → `report` + `formatResult` パターン
- 成功: `report(submission)`
- バリデーションエラー: `report(submission, { error: formatResult(result) })`
- カスタムエラー: `report(submission, { error: { formErrors: [...] } })`

## トラブルシューティング

型エラーが発生した場合：
1. future API の使い方が正しいか確認（スキーマを第一引数に渡す）
2. スキーマと `defaultValue` の型が一致しているか確認
3. サーバー側で `parseSubmission` + `report` を使っているか確認
4. `ConformAction` の型定義が `@conform-to/react/future` からインポートされているか確認

※ `any` 型での回避は禁止（詳細は `docs/no-any-type.md` 参照）

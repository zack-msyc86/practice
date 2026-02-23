# Storybook play 関数のクエリ

play 関数内で DOM 要素を取得するときは `getByRole` ではなく `findByRole` を使う。

```ts
// NG
const input = canvas.getByRole('combobox');

// OK
const input = await canvas.findByRole('combobox');
```

`getByRole` は呼び出し時点で要素が見つからなければ即エラーになる。
`findByRole` は要素が現れるまでリトライするため、ref コールバックや非同期の属性付与を待てる。

Chromatic 等の CI 環境ではローカルより初期化タイミングが遅れることがあり、`getByRole` だとローカルでは通るが CI では落ちるケースが起きる。

# Storybook スナップショット向け Story 設計

- 1 Story = 1 視覚状態。play 関数で操作して状態を作る
- 親の Story では子の詳細テストをしない（stub でよい）
- Portal 内要素は `within(canvasElement.ownerDocument.body)` で検索する
- play 関数内で `setTimeout` / `new Promise(resolve => setTimeout(...))` 等の時間待ちを使わない。非同期要素の待機には `findByText` / `findByRole` 等の Testing Library の非同期クエリを使う

# ESLint のみ（Prettier なし）

フォーマットも含めて ESLint だけで完結させる。Prettier は使わない。
ESLint だけで整形もルール適用も十分にできるため、ツールを分ける必要がない。

設定は [@praha/eslint-config](https://github.com/praha-inc/eslint-config) を使用。
`define()` で必要なパッケージ（common, javascript, style, typescript, react, next 等）を合成して使う。

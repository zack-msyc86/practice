# ESM のみ

ESM を使う。CJS はなるべく避ける。
`package.json` の `"type"` は常に `"module"`。

## 理由

ESM は言語標準のモジュールシステム。CJS との混在はトラブルの原因になるため、統一する。

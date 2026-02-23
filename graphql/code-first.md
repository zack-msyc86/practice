# GraphQL: コードファースト

GraphQL スキーマはコードファーストで定義する。スキーマファーストは使わない。

## 理由

スキーマファーストでは field resolver の親型（parent）が構造的に型安全にならない。
スキーマ定義（SDL）と resolver 実装が分離しているため、resolver が受け取る parent の型を正しく推論できず、any や手動の型注釈に頼ることになる。

コードファースト（[Pothos](../libraries/pothos/) 等）では型定義と resolver が同じコード上にあるため、parent の型が自然に推論される。

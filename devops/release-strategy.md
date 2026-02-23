# リリース戦略

リリース用のブランチは分けない。

- **staging**: main ブランチに追従してデプロイ
- **production**: GitHub のリリースを作成してデプロイ

## Feature Flag

この戦略の課題は、未完成の機能が main に含まれること。
Feature Flag を使えば大体解決できる。未完成の機能は Flag で隠し、main に安全にマージし続ける。

ブランチを長期間分けて管理するコストより、Feature Flag で制御する方がシンプル。

# Storybook + Playwright による動作確認

コンポーネント実装後は Storybook でレンダリングを確認し、playwright-cli で操作テストを行う。

```bash
# Storybook を起動（ポート 6006）
pnpm storybook

# playwright-cli でストーリーを開いて操作確認
playwright-cli open "http://localhost:6006/?path=/story/..."
```

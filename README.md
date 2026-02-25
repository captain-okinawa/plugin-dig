# plugin-dig

Dig – Cursor 用プラグイン。計画の曖昧さを構造化された質問で解消します。

## 含まれるプラグイン

- **dig**: 計画ファイルを読み、不明点を洗い出し、AskUser で 2〜4 問の構造化質問を行い、回答後に Decisions と Next Steps を出力します。

## 使い方

1. Cursor の **Settings** → **Plugins** で「Add plugin」をクリックし、次のいずれかを指定します。
   - **このリポジトリ全体**: リポジトリルート（このフォルダ）のパスを指定すると、`.cursor-plugin/marketplace.json` に登録されたプラグインが利用できます。
   - **dig のみ**: `plugins/dig` フォルダのパスを指定すると、dig だけがインストールされます。
2. チャットで **`/dig`** を実行して、計画の明確化を開始します。

詳細は [plugins/dig/README.md](plugins/dig/README.md) を参照してください。

## 開発・提出

- バリデーション: リポジトリルートで `node scripts/validate-template.mjs` を実行し、通過することを確認してください。
- マーケットプレース提出: [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish) でこのリポジトリの URL を提出してください。

## ライセンス

kuuさんがClaudeCodeのプラグインで実装していただいたものを参考にcursorでも利用できるように作成いたしました。
https://github.com/fumiya-kume/claude-code/tree/master/dig

GPL-3.0（dig プラグインと同様）


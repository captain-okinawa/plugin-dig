# plugin-dig

Dig - Cursor 向けのプラグインで、計画や要件の曖昧さを構造化した質問で解消します。

## 含まれるプラグイン

- **dig**: 計画ファイルを読み取り、曖昧点を抽出して AskUser で 2-4 個の選択肢質問を生成し、意思決定と次の作業を整理します。

## 使い方

1. Cursor の **Settings** → **Plugins** からプラグインを追加します。
   - **リポジトリ全体**: このリポジトリのルートを指定し、`.cursor-plugin/marketplace.json` を読み込ませます。
   - **dig のみ**: `plugins/dig` を指定します。
2. チャットで **`/dig`** を実行します。

詳細は `plugins/dig/README.md` を参照してください。

## 検証

- バリデーション: `node scripts/validate-template.mjs`

## マーケットプレイス公開

- 公開方法は Cursor の公式ガイドに従います。

## ライセンス

GPL-3.0（元の dig プラグインと同一）

## クレジット

- 元の dig プラグイン（Claude Code 版）
  - https://github.com/fumiya-kume/claude-code/tree/master/dig

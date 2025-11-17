# test-document プロジェクト概要

## プロジェクトについて

このディレクトリは、**Mintlify スターターキット**を使用して作成されたドキュメントサイトのリソースです。Mintlifyは、美しく機能的な技術ドキュメントを簡単に作成・公開できるプラットフォームです。

## プロジェクト構成

### 📁 ディレクトリ構造

```
test-document/
├── 📄 docs.json                    # メイン設定ファイル（ナビゲーション、テーマ、色など）
├── 📄 index.mdx                    # ホームページ（イントロダクション）
├── 📄 quickstart.mdx               # クイックスタートガイド
├── 📄 development.mdx              # 開発環境のセットアップガイド
├── 📄 README.md / README.ja.md     # プロジェクトのREADME
├── 📄 LICENSE                      # ライセンスファイル
├── 🖼️ favicon.svg                  # ファビコン
│
├── 📁 essentials/                  # コンテンツ作成の基本
│   ├── markdown.mdx                # Markdown構文ガイド
│   ├── code.mdx                    # コードサンプルの書き方
│   ├── images.mdx                  # 画像の使用方法
│   ├── navigation.mdx              # ナビゲーション設定
│   ├── settings.mdx                # サイト設定のカスタマイズ
│   └── reusable-snippets.mdx       # 再利用可能なスニペット
│
├── 📁 ai-tools/                    # AIツール連携ガイド
│   ├── cursor.mdx                  # Cursor設定ガイド
│   ├── claude-code.mdx             # Claude Code設定
│   └── windsurf.mdx                # Windsurf設定
│
├── 📁 api-reference/               # APIリファレンス
│   ├── introduction.mdx            # APIドキュメント概要
│   ├── openapi.json                # OpenAPI仕様ファイル
│   └── endpoint/                   # APIエンドポイント例
│       ├── get.mdx                 # GETエンドポイント
│       ├── create.mdx              # POSTエンドポイント
│       ├── delete.mdx              # DELETEエンドポイント
│       └── webhook.mdx             # Webhookエンドポイント
│
├── 📁 images/                      # 画像リソース
│   ├── hero-dark.png               # ダークモードヒーロー画像
│   ├── hero-light.png              # ライトモードヒーロー画像
│   └── checks-passed.png           # デプロイ成功画像
│
├── 📁 logo/                        # ロゴファイル
│   ├── dark.svg                    # ダークモードロゴ
│   └── light.svg                   # ライトモードロゴ
│
└── 📁 snippets/                    # 再利用可能なコンテンツ
    └── snippet-intro.mdx           # スニペット例
```

## 主要機能

### 1. ドキュメントサイトの構成

#### ナビゲーション構造（[`docs.json`](docs.json:1)で定義）

**Guidesタブ:**
- **Getting started** - 初期設定とクイックスタート
  - [`index.mdx`](index.mdx:1) - イントロダクション
  - [`quickstart.mdx`](quickstart.mdx:1) - 3ステップのクイックスタート
  - [`development.mdx`](development.mdx:1) - ローカル開発環境

- **Customization** - サイトのカスタマイズ
  - [`essentials/settings.mdx`](essentials/settings.mdx:1) - サイト設定
  - [`essentials/navigation.mdx`](essentials/navigation.mdx:1) - ナビゲーション設定

- **Writing content** - コンテンツ作成
  - [`essentials/markdown.mdx`](essentials/markdown.mdx:1) - Markdown構文
  - [`essentials/code.mdx`](essentials/code.mdx:1) - コードサンプル
  - [`essentials/images.mdx`](essentials/images.mdx:1) - 画像の使用
  - [`essentials/reusable-snippets.mdx`](essentials/reusable-snippets.mdx:1) - 再利用可能なスニペット

- **AI tools** - AIツール連携
  - [`ai-tools/cursor.mdx`](ai-tools/cursor.mdx:1) - Cursor設定
  - [`ai-tools/claude-code.mdx`](ai-tools/claude-code.mdx:1) - Claude Code設定
  - [`ai-tools/windsurf.mdx`](ai-tools/windsurf.mdx:1) - Windsurf設定

**API referenceタブ:**
- **API documentation**
  - [`api-reference/introduction.mdx`](api-reference/introduction.mdx:1) - API概要

- **Endpoint examples**
  - [`api-reference/endpoint/get.mdx`](api-reference/endpoint/get.mdx:1) - GETリクエスト
  - [`api-reference/endpoint/create.mdx`](api-reference/endpoint/create.mdx:1) - POSTリクエスト
  - [`api-reference/endpoint/delete.mdx`](api-reference/endpoint/delete.mdx:1) - DELETEリクエスト
  - [`api-reference/endpoint/webhook.mdx`](api-reference/endpoint/webhook.mdx:1) - Webhook

### 2. テーマとデザイン

[`docs.json`](docs.json:1)で設定されているテーマ:
- **テーマカラー**: Mintグリーン系
  - Primary: `#16A34A`
  - Light: `#07C983`
  - Dark: `#15803D`
- **ロゴ**: ライト/ダークモード対応
- **ファビコン**: カスタムSVG

### 3. 統合機能

#### コンテキストメニュー（[`docs.json`](docs.json:103-113)）
- コピー機能
- 表示機能
- AIツール連携:
  - ChatGPT
  - Claude
  - Perplexity
  - MCP
  - Cursor
  - VSCode

#### グローバルリンク
- [Mintlifyドキュメント](https://mintlify.com/docs)
- [Mintlifyブログ](https://mintlify.com/blog)

#### ソーシャルメディア
- X (Twitter)
- GitHub
- LinkedIn

## 開発ワークフロー

### ローカル開発

1. **Mintlify CLIのインストール:**
   ```bash
   npm i -g mint
   ```

2. **開発サーバーの起動:**
   ```bash
   mint dev
   ```
   - ローカルプレビュー: `http://localhost:3000`
   - 変更は自動的に反映されます

3. **カスタムポートの使用:**
   ```bash
   mint dev --port 3333
   ```

### デプロイメント

1. **GitHubアプリのインストール:**
   - [ダッシュボード](https://dashboard.mintlify.com/settings/organization/github-app)からインストール

2. **自動デプロイ:**
   - デフォルトブランチへのプッシュで自動的に本番環境にデプロイ

### ユーティリティコマンド

- **CLIの更新:**
  ```bash
  npm mint update
  ```

- **リンクの検証:**
  ```bash
  mint broken-links
  ```

## 技術スタック

- **フレームワーク**: Mintlify
- **コンテンツ形式**: MDX (Markdown + JSX)
- **設定**: JSON
- **API仕様**: OpenAPI 3.0
- **必要環境**: Node.js v19以上

## Mintlifyコンポーネント

このプロジェクトでは、以下のMintlifyコンポーネントを使用できます:

### 情報表示コンポーネント
- `<Note>` - 補足情報
- `<Tip>` - ベストプラクティス
- `<Warning>` - 重要な注意事項
- `<Info>` - 中立的な情報
- `<Check>` - 成功確認

### 構造コンポーネント
- `<Card>` / `<CardGroup>` - カード表示
- `<Columns>` - 複数カラムレイアウト
- `<Steps>` / `<Step>` - 手順の表示
- `<Tabs>` / `<Tab>` - タブ切り替え
- `<Accordion>` / `<AccordionGroup>` - 折りたたみ可能なコンテンツ

### コードコンポーネント
- `<CodeGroup>` - 複数言語のコード例
- `<RequestExample>` - APIリクエスト例
- `<ResponseExample>` - APIレスポンス例

### APIドキュメントコンポーネント
- `<ParamField>` - パラメータ定義
- `<ResponseField>` - レスポンスフィールド定義
- `<Expandable>` - ネストされたフィールド

### メディアコンポーネント
- `<Frame>` - 画像のフレーム
- `<video>` - 動画埋め込み
- `<Tooltip>` - ツールチップ

## AIツール連携

このプロジェクトには、以下のAIツールとの連携ガイドが含まれています:

1. **Cursor** ([`ai-tools/cursor.mdx`](ai-tools/cursor.mdx:1))
   - プロジェクトルール設定
   - Mintlifyコンポーネントの使用方法
   - 技術文書作成のベストプラクティス

2. **Claude Code** ([`ai-tools/claude-code.mdx`](ai-tools/claude-code.mdx:1))
   - Claude連携設定

3. **Windsurf** ([`ai-tools/windsurf.mdx`](ai-tools/windsurf.mdx:1))
   - Windsurf連携設定

## ベストプラクティス

### コンテンツ作成
1. すべてのページにYAMLフロントマター（title、description）を含める
2. 明確で具体的な見出しを使用
3. コード例は完全で実行可能なものを提供
4. 画像には説明的なalt textを含める
5. 手順は`<Steps>`コンポーネントで構造化

### コード例
- 実際に動作するコード例を提供
- エラーハンドリングを含める
- プレースホルダーではなく現実的なデータを使用
- 期待される出力を示す

### アクセシビリティ
- 適切な見出し階層を維持
- 画像に説明的なalt textを使用
- リンクテキストは具体的に
- 十分な色のコントラストを確保

## トラブルシューティング

### 開発環境が起動しない
```bash
mint update
```
最新バージョンのCLIがインストールされていることを確認

### ページが404として読み込まれる
有効な[`docs.json`](docs.json:1)があるフォルダで実行していることを確認

### "sharp"モジュールエラー
1. CLIをアンインストール: `npm remove -g mint`
2. Node.js v19以上にアップグレード
3. CLIを再インストール: `npm i -g mint`

### 不明なエラー
デバイスのルートで`~/.mintlify`フォルダを削除し、`mint dev`を再実行

## リソース

- [Mintlify公式ドキュメント](https://mintlify.com/docs)
- [Mintlifyコミュニティ](https://mintlify.com/community)
- [Mintlifyブログ](https://mintlify.com/blog)
- [顧客事例](https://mintlify.com/customers)
- [CLIチェンジログ](https://www.npmjs.com/package/mintlify?activeTab=versions)

## サポート

- **メール**: hi@mintlify.com
- **ダッシュボード**: https://dashboard.mintlify.com
- **GitHub**: https://github.com/mintlify

## ライセンス

このプロジェクトのライセンス情報は[`LICENSE`](LICENSE:1)ファイルを参照してください。
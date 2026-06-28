# 神田無垢食堂 — Vercelデプロイ手順

## 準備

1. **Vercelアカウントを作成**
   https://vercel.com にアクセスしてアカウントを作成してください

2. **GitHubにプッシュ**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

## デプロイ方法

### 方法1: Vercel UIから（推奨）

1. https://vercel.com/dashboard にログイン
2. 「Add New...」→「Project」をクリック
3. GitHubリポジトリを選択
4. 設定を確認（デフォルトで問題ありません）
5. 「Deploy」をクリック

### 方法2: Vercel CLIから

```bash
# Vercel CLIをインストール
npm install -g vercel

# プロジェクトディレクトリで実行
vercel
```

## 設定内容

- **ビルド設定**: なし（静的ファイルのため）
- **ルート**: デフォルト（`/`）
- **環境変数**: なし

## デプロイ後

デプロイが完了すると、Vercelが自動的に以下を提供します：

- 本番用URL（例: `https://kanda-muku-shokudo.vercel.app`）
- プレビューURL（各プルリクエスト）
- 自動更新（GitHubにプッシュされるたび）

## トラブルシューティング

- **404エラー**: `vercel.json` が正しくアップロードされているか確認
- **画像が表示されない**: `assets/` フォルダがアップロードされているか確認
- **キャッシュの問題**: Vercelダッシュボードから「Redeploy」を実行

## カスタムドメイン設定

Vercelダッシュボード → Project Settings → Domains から、カスタムドメインを設定できます。

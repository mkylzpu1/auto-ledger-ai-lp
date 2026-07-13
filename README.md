# 家計簿アシスタント LP

## デプロイ方法（GitHub Pages）

1. このフォルダの中身をリポジトリのルートにそのまま push してください（ブランチ: `main`）。
2. リポジトリの **Settings → Pages** を開き、「Build and deployment」の **Source** を `GitHub Actions` に設定してください（最初の1回だけ必要です）。
3. `main` ブランチに push するたびに `.github/workflows/deploy.yml` が自動実行され、GitHub Pages に反映されます。
4. 公開URLが決まったら、`index.html` 内の以下の箇所を実際のURLに置き換えてください（OGP画像が正しく表示されるために必要です）。
   - `<link rel="canonical" ...>`
   - `<meta property="og:url" ...>`
   - `<meta property="og:image" ...>`
   - `<meta name="twitter:image" ...>`

## ファイル構成

```
index.html                 ページ本体
site.webmanifest           PWA用マニフェスト
favicon.ico                ブラウザタブ用アイコン
assets/
  favicon-16x16.png
  favicon-32x32.png
  apple-touch-icon.png     iOSホーム画面用（180x180）
  icon-192.png / icon-512.png   PWA用アイコン
  ogp-image.png            LINE/Facebook/X共有時のカード画像（1200x630）
userGuide-kakeibo-assistant.mp4  操作説明動画
.github/workflows/deploy.yml     GitHub Pages 自動デプロイ設定
```

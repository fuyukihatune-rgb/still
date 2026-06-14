# Still

ひと呼吸、整える。アニメーションのガイドに合わせて呼吸するだけの、静かな呼吸アプリ。
Ataraxia Works がつくる、心の平静（アタラクシア）に寄り添う道具のひとつです。

- ビルド不要・1ファイル完結（`index.html` + `manifest.json` + `sw.js`）
- 記録はすべて端末内（localStorage キー `still_v1`）。広告・追跡・ログインなし。オフライン対応（PWA）
- 4つの呼吸パターン（なごみ 4-7-8 ／ ボックス 4-4-4-4 ／ さざなみ 5-5 ／ ゆったり 4-6）

## アイコンの作り直し

`icons/icon.svg` を編集したら、PNG を作り直します（ImageMagick）。

```sh
convert -background none icons/icon.svg -resize 192x192 icons/icon-192.png
convert -background none icons/icon.svg -resize 512x512 icons/icon-512.png
```

## デプロイ（Cloudflare Pages）

1. このリポジトリを Cloudflare Pages に接続
2. ビルド設定：フレームワークなし／ビルドコマンド空欄／出力ディレクトリ `/`
3. カスタムドメイン（例：`still.xdcyw.net`）を割り当て

© 2026 田中志 / Ataraxia Works

# millrect.com

Millrect の静的サイト用リポジトリです。

このリポジトリは、ランディングページ、ドキュメント、ブラウザでアプリをビルドなしで配信する構成です。

## 構成

```text
.
├── index.html          # 日本語ランディングページ
├── en/                 # 英語ランディングページ
├── app/                # ブラウザで動く Millrect 静的アプリ
├── docs/               # ドキュメント
├── packages/           # app/docs から参照する共有 JavaScript
├── samples/            # サンプルプロジェクト
├── site/               # ランディングページ用 CSS/JS/画像/フォント
├── robots.txt
└── sitemap.xml
```

## ローカル確認

静的ファイルだけで動くため、任意の静的サーバーで確認できます。

```bash
php -S 127.0.0.1:8080
```

ブラウザで以下を開きます。

```text
http://localhost:8080/
http://localhost:8080/app/
http://localhost:8080/docs/
```

## Cloudflare Pages にデプロイ

Cloudflare Pages では GitHub 連携を使い、ビルドなしの静的サイトとして配信します。

1. Cloudflare Dashboard で `Workers & Pages` を開く
2. `Create application` から `Pages` を選ぶ
3. GitHub リポジトリを接続する
4. Build settings を以下にする

```text
Framework preset: None
Build command:    （空）
Build output:     /
Root directory:   /
```

以後、Cloudflare Pages で指定した production branch に push すると自動デプロイされます。

## 公開前チェック

- `robots.txt` と `sitemap.xml` の URL が本番ドメインと一致していること
- OGP 画像やドキュメント内画像の参照先が存在すること
- `/app/`、`/docs/`、`/en/` のリンクが 404 にならないこと
- Cloudflare Pages の production branch が意図したブランチになっていること

## ライセンス

Millrect 独自のソース、文章、ブランド、画像などの権利は留保されています。
同梱している外部ライブラリとフォントは、それぞれのライセンスに従います。
詳細は [`LICENSE`](LICENSE) と [`NOTICE.md`](NOTICE.md) を参照してください。

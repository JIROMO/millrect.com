# Bundled fonts

Millrect uses **[Gen Interface JP](https://gen.typesetting.jp/)** (SIL OFL 1.1) as the sole bundled typeface for UI, in-app text, docs, and the landing page.

## Files

| Path | Format | Use |
|------|--------|-----|
| `app/fonts/GenInterfaceJP-Regular.ttf` | TTF | App UI, HarfBuzz / Core Text text engine |
| `app/fonts/GenInterfaceJP-Bold.ttf` | TTF | Bold weight |
| `docs/fonts/*.woff2` | WOFF2 | Documentation site |
| `site/fonts/*.woff2` | WOFF2 | millrect.com landing page |

Version: **0.5.0** (see [releases](https://github.com/yamatoiizuka/gen-interface-jp/releases)).

## Update

This public website repository commits the font binaries because they are served
directly by the static site and browser app.

When updating the fonts, replace the TTF files in `app/fonts/` and the WOFF2
files in `docs/fonts/` and `site/fonts/` from the same Gen Interface JP release,
then update the version above if needed.

Project fonts added via Google Fonts / Fontsource at runtime are subject to their respective licenses.

## 日本語

同梱フォントは **Gen Interface JP** のみです。

この静的サイト用リポジトリでは、配信用のフォントバイナリをコミットしています。

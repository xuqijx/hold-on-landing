[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [日本語](README.ja.md)

# Hold On（先别买）— ランディングページ

**Hold On** は、衝動買いの前にクールダウン時間を挟む iOS アプリ構想の静的ランディングページです。アプリは**まだリリースされておらず**、App Store にもありません。ページでは早期アクセス用のメールアドレスを受け付けています。

公開サイト：https://xuqijx.github.io/hold-on-landing/

## 予定している機能

1. **商品を共有**：ショッピングアプリから商品を Hold On に共有。
2. **価格に応じてクールダウン**：待ち時間は価格に比例し、高いものほど長く待ちます。
3. **あとで決める**：時間が来たら買うか見送るかを選び、使わずに済んだ金額を確認。

ページに記載の予定価格：$9.99 の買い切り、サブスクなし、広告なし。

## 構成

- `index.html` — Hold On のランディングページ（「リリース時に通知」メールフォーム、Formspree）。
- `packs/` — フリーランス向けテンプレート／キットのデジタルパック販売ページ（`/packs/`）。購入ボタンは Gumroad へ。詳細は `packs/README.md`。
- `guides/` — 長文ガイド（衝動買いのクールダウン、固定報酬案件のスコープクリープなど、`/guides/`）。
- `favicon.ico`、`favicon-32.png` — サイトアイコン。
- `robots.txt`、`sitemap.xml`。

## ローカルで確認

ビルド不要：

```bash
python3 -m http.server 8765
# http://127.0.0.1:8765/ を開く
```

注：アイコンのパスは GitHub Pages のプロジェクト接頭辞 `/hold-on-landing/` を使うため、ローカルのルート配信では表示されない場合があります。

## メールフォーム

`index.html` のフォームは Formspree（`https://formspree.io/f/xqppdwdw`）に送信します。自分用にする場合はフォームの `action` を置き換えてください。収集したメールリストはこのリポジトリにコミットしないでください。

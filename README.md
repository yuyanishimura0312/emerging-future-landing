# emerging-future-landing

未来庵 Miraian のランディングページです。NPO法人ミラツクが運営する京都・吉田の施設を紹介するシングルページサイトです。

## 公開 URL

https://miraian.emerging-future.org/

## 構成

```
emerging-future-landing/
├── index.html    # メインページ（全コンテンツ）
├── favicon.ico   # ファビコン
├── CNAME         # GitHub Pages カスタムドメイン設定
└── README.md     # このファイル
```

## デプロイ手順

GitHub Pages を使用しています。`main` ブランチへの push が即時反映されます。

```bash
git add .
git commit -m "feat: <変更内容>"
git push origin main
```

CNAME には `miraian.emerging-future.org` が設定されています。DNS 設定は別途ドメイン管理側で対応が必要です。

## コンテンツ更新方法

### テキスト・住所などの情報変更

`index.html` 内の該当箇所を直接編集してください。主なセクション構成は以下の通りです。

- Hero: タイトル・タグライン（L600 付近）
- Miraian: 施設説明・住所（L654 付近）
- Map: Google Maps 埋め込み・リンク（L681 付近）
- Access: アクセス案内（L700 付近）
- Organization: 組織概要（L755 付近）
- Contact: メールアドレス（L770 付近）

### OGP 画像の変更

`<head>` 内の以下の meta タグを更新してください。

```html
<meta property="og:image" content="画像URL">
<meta name="twitter:image" content="画像URL">
```

現在は SpaceMarket の CDN 画像を暫定利用しています。自前の画像に差し替える際は、1200x630px 程度の横長画像を推奨します。

### Google Maps の差し替え

L682 の `<iframe src="...">` の埋め込み URL を Google Maps の「共有 → 地図を埋め込む」から取得した URL に置き換えてください。

## 注意事項

- Gallery・Miraian セクションの画像は現在 SpaceMarket の CDN を参照しています。自前の画像に差し替えることを推奨します（M-1 対応待ち）。
- `<title>` の「Emerging Future」と `<h1>` の「Emerging Future」はブランド名として意図的に使用されていますが、施設名「未来庵」との整合性について確認が必要です（C-1 対応待ち）。

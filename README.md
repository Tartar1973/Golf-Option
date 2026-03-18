# Golf Journey Roulette - Secure Rakuten API Edition

この版は **APIキーをブラウザに埋め込まず**、Vercel Functions で楽天GORA APIを呼ぶ安全版です。

## ファイル
- index.html
- api/search.js
- vercel.json
- README.md

## Vercel に設定する環境変数
Project Settings → Environment Variables に次を設定してください。

- `RAKUTEN_APPLICATION_ID`
- `RAKUTEN_ACCESS_KEY`
- `RAKUTEN_AFFILIATE_ID`

## 使い方
1. このフォルダを GitHub にアップ
2. Vercel で Import
3. 上の3つの環境変数を Vercel に登録
4. 再デプロイ
5. 公開URLを開く

## ポイント
- APIキーは `api/search.js` のサーバー側だけで使います
- ブラウザのページソースにはキーは出ません
- 候補のゴルフ場名、評価、詳細URL、予約URLは楽天GORA APIから取得します

## 注意
- ブランド判定は公式一覧ベースの名前一致です
- `その他` は評価3.8以上だけ残すようにしています

# 一枚で整える β版

写真はアップロードせず、写真を見ながら入力した「今日のひとこと」から、Instagram投稿文・短い一言・ハッシュタグ・Google Keep用まとめを作る簡易アプリです。

## ファイル

- `index.html`：Cloudflare Pages に置く画面ファイル
- `worker.js`：Cloudflare Workers で OpenAI API に接続する処理

## 使い方の流れ

1. Cloudflare Pages に `index.html` を公開する
2. Cloudflare Workers に `worker.js` を設定する
3. Workers の環境変数に `OPENAI_API_KEY` を設定する
4. Pages 側から `/api/generate` にアクセスできるようにルーティングする

## 保存の考え方

このβ版には本格的な保存機能はありません。
生成した文章は「Google Keep用にコピー」でコピーし、Google Keepに貼り付けて、写真を自分で追加する想定です。
大切な文章は、Google KeepからGoogleドキュメントにコピーして長期保存するのがおすすめです。

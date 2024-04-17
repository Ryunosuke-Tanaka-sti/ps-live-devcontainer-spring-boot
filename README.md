# PS Live デブコン祭り：Java全く知らんエンジニアがSpring Bootの環境をdevcontainer化する

pullしてdevcontainerで起動すれば実行できます。

## プロジェクト要件

| 対象                  | バージョン |
| --------------------- | ---------- |
| JDKバージョン         | 21         |
| Spring Bootバージョン | 3.2.4      |
| ビルドツール          | Maven      |
| プロジェクトタイプ    | Java       |

- 拡張機能
  - Spring Web：Web開発
  - Spring Boot Dev Tools：ホットリロード

## 資料

発表資料：assets/PS Live デブコン祭り-Spring boot.pdf

- [環境作成：Spring Bootの環境をダウンロード](https://gist.github.com/Ryunosuke-Tanaka-sti/ecdd0b12a239111c8de96372a64d8947)
  - [Spring Initializer](https://start.spring.io/)からプロジェクトを作成してダウンロードする
- [改善](https://gist.github.com/Ryunosuke-Tanaka-sti/4e1fd8447d2d8daadea215113899084b)
  - 改善１：Volume Trickを使用してビルドファイルをコンテナ内に収める
  - 改善２：非rootユーザーで実行する
  - 改善３：レイヤーキャッシュを活用して効率化する
- 起動確認
- 環境作成：devcontainerで立ち上げる

## ディレクトリ構造

```txt
.
├── .devcontainer
│   ├── Dockerfile
│   └── devcontainer.json       // devcontainer設定ファイル
├── app                         // Spring Bootプロジェクト
├── docker-compose.yml
└── README.md
```

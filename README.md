# Domus Feed
Domus FeedはデスクトップPC向けのRSSフィードリーダーアプリです。
クラウドサービスを利用せず、アプリケーションデータはローカル環境に保存されます。

Domus Feed is a desktop RSS reader application.
Application data is stored locally without using cloud services.

## スクリーンショット


## 基本機能
- RSSの検索
- RSSの登録
- 記事の表示

## 仕様
- 登録したRSSから過去14日前までの記事を取得します
- Bookmarkしていない記事は取得してから7日前までの記事を表示します
- Bookmarkしている記事は取得日に関わらず表示されます

## Download
最新のインストーラーは[GitHub Releases](xxxx)ページを参照の上ダウンロードしてください。


## セキュリティに関する注意
### 通信について
本アプリケーションはローカル環境（`127.0.0.1`）のみで動作します。
ユーザーが登録したRSSフィード取得のために該当WebサイトへのHTTPリクエストを送信しますが、それ以外の用途でユーザーの情報を外部へ送信することはありません。

### セキュリティレポート
Virus TotalおよびCargo Auditでチェックを実施しています。
詳細なレポートは[security/report.md](security/report.md)をご覧ください。


## ライセンス
All rights reserved.

本リポジトリに含まれる成果物の再配布、改変、解析などは許可していません。

## サポート
インストールや実行時の問題については本リポジトリの[GitHub Issues](https://github.com/kitataku/domus-feed-releases/issues)よりご連絡ください。


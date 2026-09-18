# CUT CLASS — Claude Code × CapCut 動画自動編集講座

公開サイトの最新版を、GitHub・Vercelへ移せる形にまとめたファイルです。
18レッスン、図解、編集前後の切り替え、指示文コピー、画像、スタイルを含みます。
このサイト自体は学習用ガイドであり、動画編集を実行するサービスではありません。

## 1. ZIPを解凍

WindowsはZIPを右クリックして「すべて展開」。MacはZIPをダブルクリック。
解凍すると、次の3つが見えます。

- public：サイト本体。中にindex.html、画像、デザイン・動作のファイルがあります。
- vercel.json：Vercel向けの公開設定。変更不要。
- README.md：このガイド。

## 2. GitHubへアップロード

1. GitHubで新しいリポジトリを作成。名前の例：cut-class。
2. ファイルのアップロード画面を開く（Add file → Upload files。空のリポジトリでは「uploading an existing file」）。
3. **解凍した中身のpublicフォルダ・vercel.json・README.mdをまとめて**ドラッグしてアップロード。
4. Commit changesで保存。

ZIP自体や、解凍後の外側のフォルダをそのままアップロードしないでください。
GitHubの一番上にpublicフォルダとvercel.jsonが並んでいれば正しい配置です。
public内のassetsフォルダも省略せず、フォルダ構造を保ってアップロードします。

## 3. Vercelで公開

1. Vercelにログインして、新しいプロジェクトを追加。
2. GitHubを連携し、作成したリポジトリを選択してImport。
3. Framework Presetは「Other」。Root Directoryはリポジトリの最上位のまま。
4. 同梱のvercel.jsonで、ビルド不要・公開フォルダpublicを指定済みです。
5. Deployを押し、完了後に表示されるURLを開きます。

設定を手動で求められた場合：Build Commandは空欄、Output Directoryはpublic。
追加のパッケージ導入、APIキー、データベースは不要です。
この一式は公開準備用です。GitHubへのアップロードやVercelでの実際の公開はまだ行っていません。

## 公開後に確認

- トップと「編集方法を選ぶ」が表示される
- レッスンを切り替えられる
- 編集前／編集後のボタンが動く
- 指示文をコピーできる
- 参考画像を拡大できる
- スマートフォンで文字と図が読みやすい

## 中身を変更するとき

public内のファイルを変更してGitHubへ保存します。
Git連携の自動デプロイが有効なら、Vercelが更新を反映します。

| ファイル | 内容 |
|---|---|
| public/index.html | サイトの入口 |
| public/content.js | 基本講座と指示文 |
| public/guide.js | 追加講座・用語・チャット編集 |
| public/visual.js | 図解とレッスンの視覚表示 |
| public/app.js | ページ切り替え・コピー・画像拡大 |
| public/*.css | デザインとアニメーション |
| public/assets/ | 同梱の参考画像7点 |

## 画像・外部読み込みについて

元サイトと同様、一部の公式参考画像とGoogle Fontsは外部サイトから読み込みます。
完全なオフライン版ではありません。外部画像が表示されないときは、掲載元のリンクから確認してください。
参考画像の掲載元・帰属表示はサイト内に保持しています。第三者の画像や商標の権利は各権利者に帰属します。
ChatGPT Sites固有の設定、認証情報、作業用ファイル、Git履歴は同梱していません。

## 公式の説明

- GitHubでファイルをアップロード：https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
- Vercelの静的サイト設定：https://vercel.com/docs/builds/configure-a-build

作成日：2026年9月18日

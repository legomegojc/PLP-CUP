# PLP CUP OBSオーバーレイ

GitHub Pagesの操作画面からFirebase Realtime Databaseへ試合情報を保存し、OBSのブラウザソースへリアルタイム表示します。

## 1. Firebaseの設定

1. Firebase Consoleの「Authentication」→「ログイン方法」で「メール/パスワード」を有効にします。
2. 「Authentication」→「ユーザー」で操作担当者のメールアドレスとパスワードを登録します。
3. Realtime Databaseの「ルール」に `database.rules.json` の内容を貼り付けて公開します。

パスワードはGitHubのファイルには書きません。操作画面で入力します。

## 2. GitHubへ配置

このフォルダ内のファイルを、PLP-CUPリポジトリのルートへ同じ名前でアップロードしてください。

## 3. 使用URL

- 操作画面：`https://legomegojc.github.io/PLP-CUP/?room=main`
- OBS：`https://legomegojc.github.io/PLP-CUP/overlay.html?room=main`

OBSではブラウザソースを追加し、幅1280・高さ720に設定します。`overlay.html` は透明背景で文字だけを表示します。操作画面内のプレビューに限り `background.png` を表示します。

## 4. 複数試合を分ける場合

操作画面とOBSの両方で同じ `room` を指定します。

- 操作画面：`?room=match-a`
- OBS：`overlay.html?room=match-a`

使用できるルーム名は半角英数字、ハイフン、アンダースコアです。

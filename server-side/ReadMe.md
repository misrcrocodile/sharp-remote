# Websocket server base on Nodejs

## 1. Node.js / npmをインストールする（for Windows）

### インストーラーをダウンロードする。

Node.jsのHP（以下のURL）よりインストーラーをダウンロードし、インストールしてください。
```
https://nodejs.org/en/download/
```

### インストール完了を確認する
コマンドプロンプトからインストールされたNode.jsとnpmを確認する。
以下のコマンドより、Node.jsが入っていることとバージョンを確認する。

```
$node --version
v6.11.1
```

以下のコマンドより、npmが入っていることとバージョンを確認する。
```
$npm --version
v3.10.10
```

## 2. パーケージをインストールする。
コマンドプロンプトから下記のコマンドを実行します。

```
$cd server-side
$npm install
$npm start

```
## 3. Herokuにアップロードする
LANで使うように、ステップ２は十分です。どこでも、サーバーを利用できるように、インターネットで公開サーバーにアップロードが必要です。Herokuはインターネットの無料サーバーを使います。

### Herokuに登録する
まずはHerokuに登録しなければなりません。以下のリンクより、登録してください。
```
https://signup.heroku.com/login
```

### Herokuをインストールする
HerokuのHP（以下のURL）よりインストールを参考して、インストールしてください。
```
https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up
```

### アカウント認証

Herokuをインストールしたら、コマンドプロンプトを入力しましょう。
```
$ heroku login
Enter your Heroku credentials.
Email: adam@example.com
Password (typing will be hidden):
Authentication successful.
```
### アプリ作成
作成するアプリを置くディレクトリを作成します。
```
$ mkdir helloHeroku
$ cd helloHeroku
```
server-sideフォルダーの内容はすべてを作成されたHelloHerokuにコピーしてください。

### Gitリポジトリ初期化
Herokuでは、アプリケーションごとにGitを使ってリモートリポジトリへプッシュする必要があるので、リポジトリを作成し、追加、コミットします。
$ git commit -m " "のメッセージは何でも大丈夫です。

```
$ git init
$ git add .
$ git commit -m "hello heroku commit"
```
### Herokuにアプリ作成
Herokuに新しいアプリケーションを作成します。
このとき、名前指定をしなければ自動的に名前がつけられます。名前はあとからでも変更可能なので、ここは指定無しでいきます。

```
$ heroku create
Creating app... done, stack is cedar-14
https://xxxxxxxxxx.herokuapp.com/ | https://git.heroku.com/xxxxxxxxxx.git
```
**注意：ウェブクライアント設定のときに、作成したアプリのリンクを使いますので、作成されたリンクをメモしてください**
```
https://xxxxxxxxxx.herokuapp.com/
```
### アプリをデプロイ

先ほど作成したアプリをデプロイします。

```
$ git push heroku master
Counting objects: 4, done.

〜 略 〜

remote: Verifying deploy... done.
To https://git.heroku.com/xxxxxxxxxxxxxxx.git
 * [new branch]      master -> master
```
こんな感じになればOKです！

## 4. 参考
- windowsにNode.jsをインストールする - https://qiita.com/Masayuki-M/items/840a997a824e18f576d8
- Getting Started on Heroku with Node.js - https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up
- Heroku初心者がHello, Herokuをしてみる - https://qiita.com/Arashi/items/b2f2e01259238235e187
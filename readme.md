

# サーバーサイドと疎通できる簡易サーバーです。


## 導入方法

1. node.jsをインストールしてください。

https://nodejs.org/ja
推奨版を使っておけば動くハズ。


### yarnインストール（このブロックはやってもやらなくてもいい。）
一応推奨

https://classic.yarnpkg.com/en/docs/install#windows-stable

yarnをインストールする。
AlternativesのClick to expand をクリックしてOSを選択する。
そうすると下記の図のようにガイドが表示されると思います。

<img width="644" alt="yarn-install" src="https://github.com/kinachan/server-mock/assets/20530743/f2473a00-6703-4545-9141-ea833397275e">

__英語むずいと思うけど、翻訳かけて読んでね！！__ 

__教える自信なかったら事前に読んでね！__ 


## 確認コマンド

```
# ターミナルを開いて下記を実行
# node.js (npmというパッケージマネージャが自動的にインストールされています)

node -v
npm -v

# yarnもインストールしてる場合
yarn -v
```

## 実行準備

Gitからソースをクローンします。

```
npm install

# yarnをインストールしてる場合（↑か↓のどちらかだけでOK）

yarn install
```

↑のコマンドは一度だけでOK

## 起動

```
npm run start

# or 

yarn run start
```

コマンドに
```
\{^_^}/ hi!
```
が出たら成功


## 使い方

顔文字が出たログにありますが、URLにリクエストを投げるとJSONが帰ってきます。
db.jsonの中身が全容です。

例えば。。。

```
http://localhost:5656/user
全てのユーザー情報取得

http://localhost:5656/user/1
id: 1のユーザーのみ取得


登録・更新・削除も出来ます。
その際は
登録：POST
更新：PUT
削除：DELETE

を使ってください。


登録
http://localhost:5656/user
Method: POST
bodyのデータはJSON形式にする。登録したいデータをセットする
※IDは既に採番されてるものだと重複エラーとなり登録できないので、一覧からデータを見て採番しなおしてください。

更新
http://localhost:5656/user/更新したいID
Method: PUT
bodyのデータはJSON形式にする。更新後のデータをセットする。
※更新したいIDは既に採番されてるものにしないとエラーになります。

削除
http://localhost:5656/user/削除したいID
Method: DELETE

```

詳しくは
https://qiita.com/ryome/items/36da51f0f5973eab8720
この辺りを見てもらうと分かるかと思います。

# 最後に
じっくりいじくり回しちゃっても問題ないです！
（もし動かなくて戻し方分からなければ、再度クローンすれば問題ないので）


それでも分からなければ誰でも聞いてね！

よく分からない→障らないが一番悲しいです。





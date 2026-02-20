## 環境構築について

以下の環境構築方法についてはCHAPTER1の動画内で解説しています。
動画を見ながらこちらの手順を進めていただくとスムーズに環境構築ができるかと思います。

## 1.git clone後、cdコマンドを使用してcloneしたディレクトリに移動してください。
```
$ cd xxxx_xxxx_introduction_sinatra
```

<br /><br />

## 2.Docker Desktopアプリを立ち上げる
Docker Desktopアプリを立ち上げてください。

■ Windowsを使用している方
デスクトップに表示されている検索欄に「Dokcer Desktop」と打ち込んで、検索結果に表示された項目をクリックしてください。
[![Image from Gyazo](https://t.gyazo.com/teams/startup-technology/7ed4318805455ba0056ab6bd8b6d869d.gif)](https://startup-technology.gyazo.com/7ed4318805455ba0056ab6bd8b6d869d)

■ Macを使用している方
commandキー + スペースバー で Spotlight を表示したら、『docker」と打ち込んで、検索結果に表示された Docker.app をクリックしてください。
[![Image from Gyazo](https://t.gyazo.com/teams/startup-technology/e0744c7e3a010fddc4ba1057e36e89bb.gif)](https://startup-technology.gyazo.com/e0744c7e3a010fddc4ba1057e36e89bb)

<br /><br />

## 3.サーバーの起動
以下のコマンドを順番に実行してサーバーを起動してください。
```
$ docker compose build

$ docker compose up
```

<br /><br />

## 4.ブラウザにて画面が表示されるか確認する
http://localhost:3000/ にアクセスして、以下の画面が表示されるかを確認してください。

[![Image from Gyazo](https://t.gyazo.com/teams/startup-technology/ee01df5d01e3e591d583f0fc24141f06.png)](https://startup-technology.gyazo.com/ee01df5d01e3e591d583f0fc24141f06)

<br /><br /><br /><br />

### サーバーの停止

サーバーを停止する場合は、サーバーが起動しているターミナルでCtrl + C を押してください。



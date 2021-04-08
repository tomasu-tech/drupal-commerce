# Drupal Commerceのデモ環境構築

Drupal Commerce 2.xのデモサイト環境構築の説明

実行環境はPHP7.4、Drupal8.9

## Docker環境構築

Dockerイメージのビルド

```shell
docker-compose build --no-cache
```

コンテナ起動

```shell
docker-compose up -d
```

## デモサイト環境構築

コンテナに入る

```shell
docker-compose exec drupal zsh
```

デモサイトのビルド及びサーバー起動

```shell
php scripts/quickstart
```

サーバーが起動すると以下のような情報が出力されます。  
UsernameとPasswordは管理画面ログイン時に必要な情報になるので控えておく。

```shell
18/18 [▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓]
Congratulations, you installed Commerce Kickstart!

Username: admin
Password: xxxxxxxx
Drupal development server started: <http://0.0.0.0:8888>
This server is not meant for production use.
One time login url: <http://0.0.0.0:8888/user/reset/1/1617846841/nzlVsZq_Gg0iUIsr5PNQdq43ch6ZUYQQSR8ECDlOJWQ/login>
Press Ctrl-C to quit the Drupal development server.
```

## ブラウザからデモサイトの確認

ブラウザに`localhost`と入力するとデモサイトを見ることができる。

管理画面への遷移は画面右上の`Login`から。

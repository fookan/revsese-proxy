# 概要
- dockerでnginxを利用してリバースプロキシをする
- nginxでbasic 認証をかける

## 使い方
1. docker imageをビルド
    ```
    docker-compose build
    ```
2. docker imageを実行
    ```
    docker-compose up -d
    ```
3. nginxに入ってbasic認証用のユーザーとpasswordを作成する
    ```
    docker-compose exec nginx /bin/sh
    htpasswd -c /etc/nginx/.htpasswd <user名>
    <password入力>
    ```
4. localhost:8080にアクセス

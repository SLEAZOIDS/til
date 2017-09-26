# docker-composeについて
## コマンドdocker-composeとdockerの関係

docker-composeは複数のコンテナを制御するコマンド
docker-composeはdocker-compose.ymlに準拠する。

dockerは基本的には一つのコンテナに対するコマンド。

なので、docker-composeは複数のコンテナを立ち上げたあと、
一つのコンテナを制御するときはdockerコマンドを使う（多分

```
docker-compose up

//コンテナdockertest_web_1にてrails db:create
docker exec -it dockertest_web_1 rails db:create
```

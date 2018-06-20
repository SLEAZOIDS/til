# コンテナの一括停止

```
$ docker stop $(docker ps -q)
```

# dockerのコンテナとイメージのまとめて削除

コンテナまとめて削除

```

$ docker ps #確認

$ docker rm `docker ps -a -q`

```


イメージまとめて削除

```

$ docker images #確認

$ docker rmi `docker images | sed -ne '2,$p' -e 's/  */ /g' | awk '{print $1":"$2}'`

```

イメージ消せない時(noneのやつ）
```
docker rmi $(docker images | awk '/^<none>/ { print $3 }')
```

### command

* コンテナ起動
``` cmd
$ docker-compose up -d --build
```

* コンテナ停止
``` cmd
$ docker-compose stop
```
* Gemfile更新時のライブラリ更新
```cmd
$ docker-compose exec rails bundle update
```

* コンテナを消す
```cmd
$ docker rm $(docker ps -aq)
```

* イメージを消す
```cmd
$ docker rmi [image_id]
```






* memo
 - 日が変わってdocker-compose upしてもrubyが落ちてこない。
    - 毎日作り直さないとダメなのか？(めんどくさいなそれ)
      - my/rails5.2、mysql、ruby、railsのイメージを削除して再度my/rails5.2を作り直し(Dockerの再起動も含む)
    - Dockerの再起動だけでイケる？（明日確認する）
    
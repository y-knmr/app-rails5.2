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
 - 環境依存かもしれないが、イメージを作った後、コンテナ起動がうまくいかないことがある。
   - だいたいはDocker for Windowsを再起動すれば治る。
   - 治らない場合は、my/rails5.2、mysql、ruby、railsのイメージを削除して再度my/rails5.2を作り直し(Dockerの再起動も含む)
    
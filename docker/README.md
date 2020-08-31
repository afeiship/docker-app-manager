# admin
> 直接用 docker 命令测试。

## start
```shell
docker container run \
  --rm \
  --name sbw-admin \
  --volume "$PWD/sites/admin":/usr/share/nginx/html \
  --volume "$PWD/docker/admin/conf.d":/etc/nginx/conf.d \
  -p 127.0.0.1:80:80 \
  -d \
  nginx
```

## stop
```shell
# stop container
docker container stop sbw-admin
# copy config(just for test)
docker container cp sbw-admin:/etc/nginx .tmp
```

## remove all <none> images
```shell
docker rmi $(docker images --filter "dangling=true" -q --no-trunc) --force
```

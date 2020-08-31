# sites
> 这个通常会存在于另一个 docker 容器里。


## hosts
```shell
127.0.0.1	site1.moban.work
127.0.0.1	site2.moban.work
```

## sites
- http://site1.moban.work/
- http://site2.moban.work/


## docker operations
- docker rmi $(docker images --filter "dangling=true" -q --no-trunc) --force

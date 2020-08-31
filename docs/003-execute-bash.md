# execute bash


## list images
$ docker ps | awk '{print $11}'
~~~
0.0.0.0:3000->80/tcp
docker-app-manager_node_1
docker-app-manager_admin_1
docker-app-manager_web_1
~~~

## exec cmd
```shell
docker exec -it docker-app-manager_web_1 /bin/bash
```









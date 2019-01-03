# TODO App

### Create dev env
P139 3.5 コンテナ配置戦略

```
$ docker-compose up -d
$ docker container exec -it manager docker swarm init
$ docker container exec -it worker01 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it worker02 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it worker03 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it manager docker node ls // For check
```

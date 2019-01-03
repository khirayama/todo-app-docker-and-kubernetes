# TODO App
P163 Swarmによる実践的なアプリケーション構築

### Create dev env
P139 3.5 コンテナ配置戦略

```
$ docker-compose up -d
$ docker container exec -it manager docker swarm init
$ docker container exec -it worker01 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it worker02 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it worker03 docker swarm join --token YOUR_TOKEN manager:2377
$ docker container exec -it manager docker node ls // 確認のため -> Jump to P166
```

P167overlayネットワークの構築

```sh
$ docker container exec -it manager docker network create --driver=overlay --attachable todoapp
// Dockerホストを問わずに配置されているコンテナがあたかも同一のネットワークに所属しているように扱う
```

# dserve

用 `docker-compose` 打包了所有开发中要用的服务，持续添加中

## Servers

- postgres:10.2
- mariadb:10.2
- redis:latest
- nginx:stable

### Setup

```shell
$ git clone git@github.com:iuhoay/dserve.git
$ cd dserve
$ docker-compse up --no-start
```

### List all servers

```shell
$ dserve ps
Name                Command               State            Ports
---------------------------------------------------------------------------
mariadb    docker-entrypoint.sh mysqld      Exit 0
nginx      nginx -g daemon off;             Exit 0
postgres   docker-entrypoint.sh postgres    Exit 0
redis      docker-entrypoint.sh redis ...   Exit 0
```

### Start a server

```shell
$ docker-compse start nginx
```

### Stop

```shell
$ docker-compse stop nginx
```

# docker

- [docker-compose](docker-compose.md)
- [docker image](docker-image.md)
- [bind mount](bind-mount.md)

---

### postgres

```shell
docker run --name db -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret -p 5432:5432 -d postgres
```


### mysql

```shell
docker run --name <container-name> -e MYSQL_ROOT_PASSWORD=secret -d mysql:<tag>
```

### mongodb

```shell
docker run --name <container-name> -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=secret -p 27017:27017 -d mongo
```

### nginx

```shell
 docker run --name <container-name> -p 80:80  -v $(pwd):/etc/nginx/nginx.conf -d nginx
```
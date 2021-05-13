# wordpress-docker

## Preparation

### Edit `.env` file

Change following items:

* `MYSQL_ROOT_PASSWORD`
* `MYSQL_DATABASE`
* `MYSQL_USER`
* `MYSQL_PASSWORD`

If you want to change port number,
change following item:

* `NGINX_HOST_PORT`

### Create `.htpasswd` file

```shell
echo "<user>:$(openssl passwd -apr1 <password>)" >> "./nginx/.htpasswd"
```

## Launch Docker containers

```shell
docker-compose up -d
```

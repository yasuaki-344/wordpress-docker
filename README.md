# wordpress-docker

## Preparation

### Edit `.env` file

Change following items:

* `MYSQL_ROOT_PASSWORD`
* `MYSQL_DATABASE`
* `MYSQL_USER`
* `MYSQL_PASSWORD`

To resolve DNS name in the container, set following DNS setting:

* `NAME_SERVER`

If you run create or run the container in proxy environment,
set following environment variables:

* `HTTP_PROXY`
* `HTTPS_PROXY`
* `NO_PROXY`

If you want to change port number, change following item:

* `NGINX_HOST_PORT`

### Create `.htpasswd` file

```shell
echo "<user>:$(openssl passwd -apr1 <password>)" >> "./nginx/.htpasswd"
```

## Launch Docker containers

```shell
docker-compose up -d
```

# Docker Images

## Listing Docker images
To list Docker images run:
```bash
$ docker images

REPOSITORY         TAG               IMAGE ID       CREATED       SIZE
php                latest            e7ddddb9c714   2 weeks ago   407MB
busybox            latest            dc3bacd8b5ea   3 weeks ago   1.23MB
```


## Pull Docker images
To pull an image from the [Docker Hub](https://hub.docker.com) run:
```bash
$ docker pull php:latest
```
This will pull the latest tag of PHP

## Tagging Docker images
Docker images can be tagged
```bash
Usage:  docker image tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
```
 To tag a Docker image run
 ```bash
$ docker image tag php php:6.0   
```
To see the tagged image run
```bash 
$docker images

REPOSITORY         TAG               IMAGE ID       CREATED       SIZE
php                6.0               e7ddddb9c714   2 weeks ago   407MB
php                latest            e7ddddb9c714   2 weeks ago   407MB
busybox            latest            dc3bacd8b5ea   3 weeks ago   1.23MB
```
## Removing Docker images
To remove a Docker image run:
```bash
$ docker rmi php:6.0
Untagged: php:6.0
```

# Docker Containers

## Listing Docker containers
To list all the running containers run:
```bash
$ docker ps

CONTAINER ID   IMAGE             COMMAND                  CREATED        STATUS         PORTS                 NAMES
f8fe68658db7   api_api           "docker-php-entrypoi…"   4 weeks ago    Up 2 minutes   80/tcp, 443/tcp       api_api_1
7c842729a96b   mysql:5.7         "docker-entrypoint.s…"   4 weeks ago    Up 2 minutes   3306/tcp, 33060/tcp   api_db_1
4d826fd8ce44   gateway_gateway   "/docker-entrypoint.…"   5 months ago   Up 2 minutes   0.0.0.0:80->80/tc     gateway_gateway_1

```
To list all containers regardless of their status run:
```bash
$ docker ps -a 
CONTAINER ID   IMAGE              COMMAND                  CREATED        STATUS                            PORTS               NAMES
3837b732d7ba   api_cms            "docker-php-entrypoi…"   4 weeks ago    Exited (137) About a minute ago                       api_cms_1
f8fe68658db7   api_api            "docker-php-entrypoi…"   4 weeks ago    Up 5 minutes                      80/tcp, 443/tcp     api_api_1
7c842729a96b   mysql:5.7          "docker-entrypoint.s…"   4 weeks ago    Up 5 minutes                      3306/tcp, 33060/tcp api_db_1
4d826fd8ce44   gateway_gateway    "/docker-entrypoint.…"   5 months ago   Up 5 minutes                      0.0.0.0:80->80/tcp  gateway_gateway_1
```

To list only the container IDs run:
```bash
$ docker ps -q
f8fe68658db7
7c842729a96b
4d826fd8ce44
```
## Running Docker containers
```bash
Usage:  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```
To run a container
```bash
$ docker run -it --rm  php

Interactive shell

php >
```

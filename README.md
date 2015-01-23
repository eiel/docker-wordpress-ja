# About this Repo

This is the Git repo of the Docker image for [eiel/wordpress](https://registry.hub.docker.com/u/eiel/wordpress/). See the
Hub page for the full readme on how to use the Docker image and for information
regarding contributing and issues.

This repository fork [docker-library/wordpress](https://github.com/docker-library/wordpress).


# Usage

```
$ docker run -d --name my-mysql -e MYSQL_ROOT_PASSWORD="secret" mysql
$ docker run -d --name my-wordpress --link my-mysql:mysql -e MYSQL_ROOT_PASSWORD="secret" -p 8000:80 -v `pwd`/wordpress:/var/www/html eiel/wordpress
```

Delete container

```
$ docker stop my-wordpress my-mysql
$ docker rm my-wordpress my-mysql
```

# docker_php
docker with php extensions

## extensions
 - gd freetype mysqli pdo pdo_mysql

## run with php:apache
```
$ docker run -d -p 80:80 --name my-apache-php-app -v "$PWD":/var/www/html firesh/php:5.6-apache
```

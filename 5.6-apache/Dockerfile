FROM php:5.6-apache

RUN apt-get update -y && \
apt-get install -y libfreetype6-dev libmcrypt-dev libjpeg-dev libpng-dev && \
docker-php-ext-configure gd --enable-gd-native-ttf --with-freetype-dir=/usr/include/freetype2 --with-png-dir=/usr/include --with-jpeg-dir=/usr/include && \
docker-php-ext-install gd mysqli pdo pdo_mysql zip mcrypt


# configure apache
RUN cp /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/

# setup timezone
#ENV TZ=Asia/Shanghai
#RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

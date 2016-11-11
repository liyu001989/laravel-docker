FROM php:7.0-fpm-alpine

MAINTAINER liyu liyu001989@gmail.com

# 换为国内镜像，以加速docker image制作速度
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/' /etc/apk/repositories
RUN apk update && apk upgrade

# mcrypt 扩展
RUN apk add libmcrypt-dev
RUN docker-php-ext-install mcrypt

# gd 扩展
RUN apk add libjpeg-turbo-dev
RUN apk add libpng-dev
RUN docker-php-ext-install gd

# pdo_mysql 扩展
RUN docker-php-ext-install pdo_mysql

# bamatch
RUN docker-php-ext-install bcmath

# 安装 composer
RUN php -r "readfile('http://install.phpcomposer.com/installer');" | php -- --install-dir=/bin/ --filename=composer

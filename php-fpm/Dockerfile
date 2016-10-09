FROM php:7.0-fpm-alpine

MAINTAINER liyu liyu001989@gmail.com

# 换为国内镜像，以加速docker image制作速度
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/' /etc/apk/repositories
RUN apk update && apk upgrade

# mcrypt 扩展需要的依赖
RUN apk add libmcrypt-dev

# pdo_mysql mcrypt 扩展
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mcrypt

# 安装 composer
RUN php -r "readfile('http://install.phpcomposer.com/installer');" | php -- --install-dir=/bin/ --filename=composer

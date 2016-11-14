FROM php:7.0-fpm-alpine

MAINTAINER liyu liyu001989@gmail.com

# mcrypt 扩展
RUN apk add libmcrypt-dev
RUN docker-php-ext-install mcrypt

# gd 扩展
RUN apk add libjpeg-turbo-dev
RUN apk add libpng-dev
RUN docker-php-ext-install gd

# pdo_mysql 扩展
RUN docker-php-ext-install pdo_mysql

# 安装 composer
RUN php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/bin/ --filename=composer

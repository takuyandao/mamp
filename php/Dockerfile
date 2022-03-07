FROM php:8-apache

WORKDIR /var/www/html

RUN apt-get update \
    && apt-get install -y libonig-dev libzip-dev unzip \
    && docker-php-ext-install pdo_mysql mbstring zip bcmath \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY ./php.ini /usr/local/etc/php/php.ini
COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
FROM php:7.1.3-fpm

RUN apt-get update && apt-get install -y \
    libpng-dev \
    zip \
    libmcrypt-dev

RUN docker-php-ext-install pdo_mysql

RUN docker-php-ext-install mcrypt \
    && docker-php-ext-install gd

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

ONBUILD RUN composer update
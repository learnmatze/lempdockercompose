FROM php:8.2-fpm

# Install MongoDB extension

RUN apt-get update
RUN docker-php-ext-install pdo pdo_mysql mysqli

RUN apt-get install -y autoconf pkg-config libssl-dev
RUN pecl install mongodb
RUN docker-php-ext-enable mongodb
RUN echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/mongodb.ini

# RUN apt-get update -y && apt-get upgrade \
#     && pecl install mongodb && docker-php-ext-enable mongodb

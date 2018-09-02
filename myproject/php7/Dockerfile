FROM php:7.2.9-fpm-alpine

RUN apk add --no-cache $PHPIZE_DEPS postgresql-dev \
    && pecl install xdebug

RUN docker-php-ext-install mbstring pdo_pgsql pgsql \
   && docker-php-ext-enable xdebug

COPY ./php.ini /usr/local/etc/php/
COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

WORKDIR /var/www

CMD ["php-fpm"]

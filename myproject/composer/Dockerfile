FROM php:7.0.12

WORKDIR /tmp

RUN apt-get update -y
RUN apt-get install -y git unzip
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer
RUN composer self-update
RUN composer global require hirak/prestissimo

ENTRYPOINT ["composer"]
CMD ["--help"]
FROM php:7.2.9-cli
WORKDIR /opt/php
RUN apt-get update \
    && apt-get install -y zlib1g-dev wget git-core \
    && docker-php-ext-install zip


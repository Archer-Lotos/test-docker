FROM php:7.0-fpm

RUN apt-get update && apt-get install -y \
        curl \
        wget \
        git \
        libmcrypt-dev \
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt mbstring mysqli pdo_mysql

ADD php.ini /usr/local/etc/php/conf.d/40-custom.ini

WORKDIR /var/www/magento2

CMD ["php-fpm"]

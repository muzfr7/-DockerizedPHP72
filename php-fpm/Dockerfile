FROM php:7.2-fpm

MAINTAINER "Muzafar Jatoi <muzfr7@gmail.com>"

RUN apt-get update \
	&& apt-get install -y zlib1g-dev libpq-dev git nano libicu-dev libxml2-dev \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl \
    && docker-php-ext-install pdo pdo_mysql mysqli \
    && docker-php-ext-install zip xml

# Install Composer
RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

# Set TimeZone
RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Asia/Karachi /etc/localtime
RUN "date"

COPY php.ini /usr/local/etc/php/

WORKDIR /var/www
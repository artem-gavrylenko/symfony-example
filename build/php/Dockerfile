FROM php:7.2-apache

COPY php.ini /usr/local/etc/php/
COPY virtual-host.conf /etc/apache2/sites-available/000-default.conf
RUN a2enmod rewrite \
  && apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev zlib1g-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv zip
RUN curl --silent --show-error https://getcomposer.org/installer | php

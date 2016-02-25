FROM php:5.6-apache

COPY config/php.ini /usr/local/etc/php/
COPY sources.list /etc/apt/


RUN apt-get update && apt-get install -y \
	libicu-dev \
	libxml2-dev \
	&& rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install mysql pdo_mysql

RUN useradd cloud

COPY config/apache2.conf /etc/apache2/apache2.conf

RUN a2enmod rewrite





FROM php:7.2-apache

RUN docker-php-ext-install mysqli
# Documentação
# https://github.com/docker-library/docs/tree/master/php#configuration
# ENV APACHE_DOCUMENT_ROOT /path/to/new/root

# Use the default production configuration
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"


WORKDIR /var/www/html/

COPY ./src/ /var/www/html/

EXPOSE 80

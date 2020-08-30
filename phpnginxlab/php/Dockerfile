FROM php:7.3-fpm-stretch
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
RUN docker-php-ext-install -j$(nproc) pdo pdo_mysql
RUN apt-get update && apt-get install -y gettext
COPY docker/php-fpm/custom-entrypoint /usr/local/bin/
RUN chmod u+x /usr/local/bin/custom-entrypoint
ENTRYPOINT ["custom-entrypoint"]
RUN mkdir /var/www/html/conf/
COPY conf/*.tmp /tmp/conf/
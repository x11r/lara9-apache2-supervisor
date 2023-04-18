FROM php:8.1-apache-bullseye

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
COPY laravel-worker.conf /etc/supervisor/conf.d/

RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install less vim git mycli supervisor \
    && apt-get clean \
    && docker-php-ext-install pdo_mysql opcache \
    && a2enmod rewrite

# CMD /usr/bin/supervisord -c /etc/supervisor/supervisord.conf && /usr/sbin/apache2 -DFOREGROUND
# CMD /usr/bin/supervisord -c /etc/supervisor/supervisord.conf

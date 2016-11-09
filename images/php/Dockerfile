FROM php:5.6-fpm
RUN apt-get update && apt-get install -y libmcrypt-dev

# lumen packages
RUN apt-get install -y php5-memcached
RUN apt-get install -y libpq-dev
RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql
RUN docker-php-ext-install mcrypt mbstring tokenizer pdo pdo_pgsql
RUN apt-get install -y libz-dev libmemcached-dev
RUN pecl install memcached
RUN docker-php-ext-enable memcached 

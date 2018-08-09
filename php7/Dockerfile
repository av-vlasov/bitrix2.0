FROM phpdockerio/php72-fpm

MAINTAINER skazochnik2007

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php7.2-memcached \
    php7.2-memcache \
    php7.2-mbstring \
    php7.2-mysql \
    php7.2-intl \
    php7.2-xdebug \
    php7.2-interbase \
    php7.2-soap \
    php7.2-gd \
    php7.2-imagick \
    php7.2-mcrypt \
    php7.2-opcache \
    php7.2-zip \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
    
RUN usermod -u 1000 www-data

ADD ./php.ini /etc/php/7.2/fpm/conf.d/90-php.ini
ADD ./php.ini /etc/php/7.2/cli/conf.d/90-php.ini

RUN usermod -u 1000 www-data

WORKDIR "/var/www/bitrix"

EXPOSE 9000

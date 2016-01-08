# Composer Docker Container
FROM imega/base-builder:1.0.0

MAINTAINER k-ndeye <khadimrassoulndeye@gmail>

ENV COMPOSER_CACHE_DIR=/cache

RUN apk add --update curl \
        git \
        php-common \
        php-cgi \
        php \
        php-cli \
        php-phar \
        php-json \
        php-ctype \
        php-xml \
        php-dom \
        php-intl \
        php-mysql\
        php-pdo \
        php-openssl && \
    curl -k -sS https://getcomposer.org/installer | php -- --version=1.0.0-alpha11 --install-dir=/usr/local/bin --filename=composer && \
    apk del curl && \
    rm -rf /var/cache/apk/*

ENTRYPOINT ["/usr/local/bin/composer"]

#commande
#docker run --rm -v /var/www/local.dev/emploisn/:/data kndeye/composer
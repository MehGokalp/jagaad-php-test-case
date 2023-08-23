FROM php:8.2.9-alpine
# install extensions
RUN apk add --update linux-headers

RUN apk add  --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && pecl install xdebug-3.2.2 \
    && docker-php-ext-enable xdebug \
    && apk del -f .build-deps

RUN apk --update add --virtual build-dependencies build-base openssl-dev autoconf \
 && pecl install igbinary

# install bcmath extension
RUN docker-php-ext-install bcmath

RUN apk add icu-dev
RUN docker-php-ext-configure intl && docker-php-ext-install intl

RUN echo "expose_php=0" > /usr/local/etc/php/php.ini

ENTRYPOINT ["tail"]
CMD ["-f","/dev/null"]

FROM php:8.2.1-cli-alpine3.17

RUN apk update

RUN apk add --no-cache \
    php81-mbstring \
    php81-intl \
    php81-gd \
    php81-xsl \
    php81-iconv \
    php81-mysqli \
    php81-pgsql \
    php81-ldap \
    libzip \
    zip \
    unzip

RUN apk add --no-cache --virtual .php-extension-deps \
    oniguruma-dev \
    libpng-dev \
    libjpeg-turbo-dev \
    libzip-dev \
    freetype-dev \
    postgresql-dev \
    openldap-dev \
    libxslt-dev \
    icu-dev \
    curl && \
    docker-php-ext-install mbstring zip exif pcntl xsl intl ldap pdo_mysql pdo_pgsql pgsql && \ 
    docker-php-ext-configure gd && \
    docker-php-ext-install gd && \
    apk del .php-extension-deps



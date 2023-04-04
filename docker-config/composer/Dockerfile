FROM composer:2.4

RUN apk update

RUN apk add --no-cache \
    libxslt-dev \
    icu-dev \
    libpng-dev \
    libjpeg-turbo-dev \
    oniguruma-dev \
    libzip-dev \
    freetype-dev \
    postgresql-dev \
    openldap-dev \
    zip \
    unzip

RUN apk add --no-cache --virtual .php-extension-deps \
    libxslt-dev \
    curl && \
    docker-php-ext-install mbstring zip exif pcntl xsl intl ldap pdo_mysql pdo_pgsql pgsql && \ 
    docker-php-ext-configure gd && \
    docker-php-ext-install gd && \
    apk del .php-extension-deps




FROM composer:2.0.4

RUN apk update

RUN apk add --no-cache \
    php7-mbstring \
    php7-intl \
    php7-gd \
    php7-xsl \
    php7-iconv \
    php7-mysqli \
    php7-pgsql \
    php7-ldap \
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



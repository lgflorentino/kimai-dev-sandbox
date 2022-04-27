FROM composer:2.0.4

RUN apk update

RUN apk add --no-cache \
    oniguruma-dev \
    libpng-dev \
    libjpeg-turbo-dev \
    libzip-dev \
    freetype-dev \
    zip \
    unzip \
    php7-mbstring \
    php7-intl \
    php7-gd \
    php7-xsl \
    php7-iconv \
    php7-mysqli \
    php7-pgsql \
    libxslt-dev \
    icu-dev \
    curl

RUN docker-php-ext-install mbstring zip exif pcntl xsl intl pdo_mysqli pdo_pgsql pgsql
RUN docker-php-ext-configure gd
RUN docker-php-ext-install gd



RUN addgroup www
RUN adduser -D -s /bin/zsh -G www www
RUN addgroup www www-data
USER www

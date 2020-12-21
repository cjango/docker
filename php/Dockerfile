FROM php:7.4.13-fpm

# 安装 comopser
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

COPY ./source.ali.list /etc/apt/sources.list

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && sync && \
    install-php-extensions redis mongodb imagick opcache

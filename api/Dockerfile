
# main image
FROM php:7.4-fpm

# packages
RUN apt-get update \
    && apt-get install -y libpq-dev && docker-php-ext-install -j$(nproc) pdo_pgsql \
    && apt-get install -y libxml2-dev && docker-php-ext-install -j$(nproc) soap \
    && docker-php-ext-install -j$(nproc) bcmath \
    && rm -rf /var/lib/apt/lists/*

ARG WORKDIR
WORKDIR ${WORKDIR}

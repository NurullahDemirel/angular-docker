FROM php:8.2-fpm
# Composer kur
COPY --from=composer /usr/bin/composer /usr/bin/composer
# container ayakta kalınca php-fpm çalışsın

# Gerekli PHP eklentileri paket çalışsın diye
RUN apt-get update && apt-get install -y \
    libcurl4-openssl-dev \
    libzip-dev \
    unzip \
    && docker-php-ext-install curl
CMD ["php-fpm"]


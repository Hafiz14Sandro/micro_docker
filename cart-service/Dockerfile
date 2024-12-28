#base image
FROM php:8.2-cli

#working dir
WORKDIR /var/www/html

#copy all file
COPY . .

RUN apt-get update && apt-get install -y \
    libpq-dev \
    && docker-php-ext-install pdo pdo_pgsql
EXPOSE 3002

#S digunakan untuk menjalankan server dengan spesifik port
CMD [ "php", "-S", "0.0.0.0:3001", "-t", "public" ]
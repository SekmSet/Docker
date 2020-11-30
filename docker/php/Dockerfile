FROM php:7.4-fpm

RUN apt update && apt install -y unzip

RUN docker-php-ext-install mysqli pdo pdo_mysql opcache

WORKDIR /var/www/html/
COPY ./app /var/www/html

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer install

RUN chmod -R 777 var

CMD ["php-fpm"]
EXPOSE 9000
FROM php:7.2-apache

RUN apt-get update && apt-get install git zlib1g-dev libpng-dev -y && docker-php-ext-install mysqli gd && docker-php-ext-enable mysqli
RUN git clone https://github.com/LeedRSS/Leed /var/www/html
RUN chown -R www-data:www-data /var/www/html/*

CMD ["apache2-foreground"]

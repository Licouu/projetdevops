FROM php:7.2-apache

# Mettre à jour et installer les dépendances nécessaires, y compris libzip-dev
RUN apt-get update && apt-get install -y libzip-dev git zlib1g-dev libpng-dev && \
    docker-php-ext-install mysqli gd zip && \
    docker-php-ext-enable mysqli

# Cloner le projet LeedRSS dans /var/www/html
RUN git clone https://github.com/LeedRSS/Leed /var/www/html

# Changer les permissions du dossier
RUN chown -R www-data:www-data /var/www/html/*

# Lancer Apache en mode foreground
CMD ["apache2-foreground"]

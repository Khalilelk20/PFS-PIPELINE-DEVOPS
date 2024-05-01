# Utilisez une image PHP avec Apache
FROM php:7.4-apache

# Installation des extensions PHP nécessaires
RUN docker-php-ext-install mysqli

# Copier les fichiers de l'application dans le répertoire de travail du conteneur
COPY ./PFS /var/www/html/

# Définir les permissions sur les fichiers de l'application
RUN chown -R www-data:www-data /var/www/html/

# Exposer le port 80 pour Apache
EXPOSE 80

# Commande par défaut pour démarrer Apache
CMD ["apache2-foreground"]

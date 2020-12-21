FROM mpltr/php-apache-composer-node

## Laravel

# copy application to document root folder
# COPY ./ /var/www/html

# RUN composer install
# RUN npm install 

# change doc root to the public folder of laravel
ENV APACHE_DOCUMENT_ROOT /var/www/html/public
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
# mod_rewrite for .htaccess and headers
RUN a2enmod rewrite headers

# RUN docker-php-ext-install \
#     bz2 \
#     intl \
#     iconv \
#     bcmath \
#     opcache \
#     calendar \
#     mbstring \
#     pdo_mysql \
#     zip

# # Further 
# RUN useradd -G www-data,root -u 1000 -d /home/devuser devuser
# RUN mkdir -p /home/devuser/.composer && \
#     chown -R devuser:devuser /home/devuser  
# RUN chmod -R 777 /var/www/html

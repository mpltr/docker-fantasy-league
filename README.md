
# Install
Create .env file in client using the .env.example as template

## Stand up docker containers and enter bash in api 
```bash
    docker-compose up
    docker-compose exec api bash
```
## Install PHP dependencies and migrate db tables 
```bash
    composer install
    php artisan migrate 
```



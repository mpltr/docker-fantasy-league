
# Install

## Cloning
As the repo uses submodules, you need to ensure you clone using the following command:
```
git clone git@github.com:mpltr/docker-fantasy-league.git --recursive
```

If you have already pulled the repo and have empty submodules, use:
```
git submodule update --init
```

**Note: You won't be prompted to enter your SSH password for submodules so you need to ensure you have enabled a way for SSH or your terminal to remember your password.**

## .env
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



# laravel-9-nginx-mysql-docker

modified from https://github.com/ishaqadhel/docker-laravel-mysql-nginx-starter

## About

Project Starter For Web Application Development with Laravel 9, MySQL 5.7.16, Nginx, and Docker.

## Installation

1. Clone this repository
2. Go to project folder and run `docker-compose up -d`
3. Create .env file for laravel environment from .env.example on src folder.
4. Enter into php container shell as root `docker exec -it --user=root php /bin/sh`
5. Run `composer install`
6. Run `php artisan key:generate`
7. Set the database connection according to MySQL environment settings in the docker-compose.yml
8. Open http://127.0.0.1:8001/

## Accessing MySQL Database

1. Enter into mysql container shell as root `docker exec -it --user=root mysql /bin/sh`
2. Run `mysql -u root -p`
3. Enter password

## Troubleshoots

1. If you encounter `the stream or file could not be opened in append mode failed to open stream permission denied`

- Enter into php container shell as root
- Run `chown -R www-data:www-data /var/www`

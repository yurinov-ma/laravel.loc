## Установка из репозитория
Склонируйте репозиторий.
```sh
git clone https://github.com/yurinov-ma/laravel.loc.git
```

Перейдите в папку с проектом и установите composer-зависимости

```sh
cd laravel.loc
composer install
```
Скопируйте файл .env.example и переименуйте его в .env

```sh
cp .env.example .env
```
Сгенерируйте ключ шифрования
```sh
php artisan key:generate
```
Измените файл конфигурации .env
```php
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Имя_БД
DB_USERNAME=Вашь_логин_от_БД
DB_PASSWORD=Вашь_пароль_от_БД

SESSION_DRIVER=file
```
## Пустой проект создан командами
```sh
composer create-project laravel/laravel .
php artisan install:api
php artisan config:publish cors
php artisan stortage:link
```
В корне проекта создан файл .htaccess
```php
RewriteEngine on
RewriteRule ^(.*)$ public/$1 [L]

```
Please add the [Laravel\Sanctum\HasApiTokens]

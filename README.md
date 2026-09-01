# Laravel Picture API

REST API for a picture gallery: public listing plus Sanctum-authenticated write routes. Built as the backend for [VuePictureApi](https://github.com/dekpo/VuePictureApi).

| | |
|---|---|
| **Source** | https://github.com/dekpo/LaravelPictureApi |
| Stack | PHP, Laravel 9, Laravel Sanctum, Eloquent |

## Endpoints

| Method | Path | Auth |
|---|---|---|
| POST | `/api/register`, `/api/login` | no |
| GET / POST / … | `/api/picture` | no (resource) |
| CRUD | `/api/authpicture` | Sanctum |

`Picture` model + `PictureResource` for JSON. Register / login issue Sanctum tokens.

## Setup

```bash
composer install
cp .env.example .env && php artisan key:generate
php artisan migrate
php artisan serve
```

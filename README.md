# authorization
[![Latest Stable Version](https://poser.pugx.org/marcocastignoli/authorization/version)](https://packagist.org/packages/marcocastignoli/authorization)
[![Total Downloads](https://poser.pugx.org/marcocastignoli/authorization/downloads)](https://packagist.org/packages/marcocastignoli/authorization)
[![Latest Unstable Version](https://poser.pugx.org/marcocastignoli/authorization/v/unstable)](//packagist.org/packages/marcocastignoli/authorization)
[![License](https://poser.pugx.org/marcocastignoli/authorization/license)](https://packagist.org/packages/marcocastignoli/authorization)

A package to manage authorization for Lumen

## Dependencies

* PHP >= 7.0
* Lumen >= 5.3

## Installation via Composer

First install Lumen if you don't have it yet:
```bash
$ composer create-project --prefer-dist laravel/lumen lumen-app
```

Then install Lumen Passport (it will fetch Laravel Passport along):

```bash
$ cd lumen-app
$ composer require marcocastignoli/authorization
```

Or if you prefer, edit `composer.json` manually:

```json
{
    "require": {
        "marcocastignoli/authorization": "dev-master"
    }
}
```

### Modify the bootstrap flow (```bootstrap/app.php``` file)

```php
// Enable Facades
$app->withFacades();

// Enable Eloquent
$app->withEloquent();

// Register the service provider
$app->register(marcocastignoli\authorization\AuthorizationProvider::class);
```

### Migrate and seed the database

```bash
# Create new tables
php artisan migrate

# Seed the database
php artisan db:seed --class=marcocastignoli\\authorization\\AuthorizationSeeder
```

### Authentication system
Implement an authentication system, I suggest you to use "passport", for Lumen you can check this: https://github.com/dusterio/lumen-passport/


## License

The MIT License (MIT)
Copyright (c) 2016 Marco Castignoli

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
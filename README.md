# Advance Trust
This package inspired and extend the [![santigarcor/laratrust](https://github.com/santigarcor/laratrust)](https://github.com/santigarcor/laratrust).

[![Latest Stable Version](https://poser.pugx.org/feripratama/advancetrust/v/stable)](https://packagist.org/packages/feripratama/advancetrust)
[![Software License][ico-license]](LICENSE.md)
[![Total Downloads](https://poser.pugx.org/feripratama/advancetrust/downloads)](https://packagist.org/packages/feripratama/advancetrust)
## Install
Via composer
``` bash
$ composer require feripratama/advancetrust
```
## 1. In your config/app.php add : 

``` php
'providers' => array(

    App\Providers\EventServiceProvider::class,
    App\Providers\RouteServiceProvider::class,
    ...
    feripratama\advancetrust\advancetrustServiceProvider::class,
    Laratrust\LaratrustServiceProvider::class,
    Collective\Html\HtmlServiceProvider::class,
    'That0n3guy\Transliteration\TransliterationServiceProvider',

),
```
``` php
'aliases' => [

    'Validator' => Illuminate\Support\Facades\Validator::class,
    'View' => Illuminate\Support\Facades\View::class,
    ...
    'Laratrust'   => Laratrust\LaratrustFacade::class,
    'Form' => Collective\Html\FormFacade::class,
    'Html' => Collective\Html\HtmlFacade::class,
```
## 2. php artisan
``` bash
$ php artisan vendor:publish --tag="laratrust"
$ php artisan laratrust:setup
$ php artisan laratrust:seeder
$ php artisan migrate
$ composer dump-autoload
$ php artisan db:seed --class=LaratrustSeeder
$ php artisan serve
```
## Please run this available command after finished installation
``` bash
php artisan advancetrust:add-route
php artisan advancetrust:create-controller
php artisan advancetrust:create-view
php artisan advancetrust:version
```
If you want to customize from default UI you can made in on your blade.

### Patch's are welcome

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/:vendor/:package_name.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/:vendor/:package_name/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/:vendor/:package_name.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/:vendor/:package_name.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/:vendor/:package_name.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/:vendor/:package_name
[link-travis]: https://travis-ci.org/:vendor/:package_name
[link-scrutinizer]: https://scrutinizer-ci.com/g/:vendor/:package_name/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/:vendor/:package_name
[link-downloads]: https://packagist.org/packages/:vendor/:package_name
[link-author]: https://github.com/:author_username
[link-contributors]: ../../contributors


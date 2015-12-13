# Twitter REST Api

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Total Downloads][ico-downloads]][link-downloads]

Laravel 5.1 wrapper for the most popular PHP library for use with the Twitter OAuth REST API. https://github.com/abraham/twitteroauth

## Installation

To install, run the following in your project directory

``` bash
$ composer require mbarwick83/twitter-api
```

Then in `config/app.php` add the following to the `providers` array:

```
Mbarwick83\TwitterApi\TwitterApiServiceProvider::class
```

Also in `config/app.php`, add the Facade class to the `aliases` array:

```
'TwitterApi'    => Mbarwick83\TwitterApi\Facades\TwitterApi::class
```

## Configuration

To publish Shorty's configuration file, run the following `vendor:publish` command:

```
php artisan vendor:publish --provider="Mbarwick83\TwitterApi\TwitterApiServiceProvider"
```

This will create a twitter-api.php file in your config directory. Here you **must** enter your Twitter App Consumer Key, Consumer Secret, and Callback URL. Create your app at [https://apps.twitter.com](https://apps.twitter.com).

## Usage

**Be sure to include the namespace for the class wherever you plan to use this library**

```
use Mbarwick83\TwitterApi\Facades\TwitterApi;
```

#####Generate Authorize URL:

This generates a URL that points users to Twitter's authorization page where they can authorize your app. It lists permissions being granted and allow/deny buttons.

``` php
$url = TwitterApi::authorizeUrl();
return $url;
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/mbarwick83/twitter-api.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/mbarwick83/twitter-api.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/mbarwick83/twitter-api
[link-downloads]: https://packagist.org/packages/mbarwick83/twitter-api
[link-author]: https://github.com/mbarwick83
[link-contributors]: ../../contributors

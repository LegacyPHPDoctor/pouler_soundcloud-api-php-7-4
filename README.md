# legacyphpdoctor/pouler_soundcloud-api-php-7-4

WARNING: This repository is a PHP 7.4 compatible fork of [pouler/soundcloud-api](https://github.com/pouler/soundcloud-api).

[![Latest Stable Version](https://poser.pugx.org/pouler/soundcloud-api/v/stable)](https://packagist.org/packages/legacyphpdoctor/pouler_soundcloud-api-php-7-4)
[![Latest Unstable Version](https://poser.pugx.org/pouler/soundcloud-api/v/unstable)](https://packagist.org/packages/legacyphpdoctor/pouler_soundcloud-api-php-7-4)

# SoundCloud API PHP

This is a PHP wrapper for the [SoundCloud API](https://developers.soundcloud.com/docs/api/explorer/open-api).

## Requirements
* PHP >=8.1
* Symfony HTTP Client

## Installation
Install it using [Composer](https://getcomposer.org/):

```sh
composer require legacyphpdoctor/pouler_soundcloud-api-php-7-4
```

```php
<?php

require 'vendor/autoload.php';

$curl = new \Symfony\Component\HttpClient\CurlHttpClient();
$client = new PouleR\SoundCloudAPI\SoundCloudClient($curl);

$api = new \PouleR\SoundCloudAPI\SoundCloudAPI($client);
$api->setClientId('client.id');

// Get information about given user
$api->getUser(123456);

// Get information about current usr
$api->setAccessToken('access.token');
$api->getUser();

var_dump($result);
```


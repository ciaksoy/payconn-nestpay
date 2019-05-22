# Nestpay

**Core components for the Payconn PHP payment processing library**

[![Build Status](https://travis-ci.com/payconn/nestpay.svg?branch=master)](https://travis-ci.com/payconn/nestpay)
[![GitHub forks](https://img.shields.io/github/forks/payconn/nestpay.svg?style=plastic)](https://github.com/payconn/nestpay/network)
[![GitHub stars](https://img.shields.io/github/stars/payconn/nestpay.svg)](https://github.com/payconn/nestpay/stargazers)
[![GitHub license](https://img.shields.io/github/license/payconn/nestpay.svg)](https://github.com/payconn/nestpay)

[Payconn](https://payconn.org) is a framework agnostic, multi-gateway payment
processing library for PHP. This package implements common classes required by Payconn.

## Supported card families
* Axess
* Bonus
* Cardfinans
* Maximum
* Paraf
* World

## Supported methods
* purchase
* void

## Basic Usage
```php
use Payconn\Nestpay;

$gateway = new Nestpay(new Nestpay\Token('YOUR_CLIENT_ID', 'YOUR_USERNAME', 'YOUR_PASS'));
$response = $gateway->purchase([
    'creditCard' => new \Payconn\Common\CreditCard('Holder Name', '4355084355084358', '26', '12', '000'),
    'amount' => 1,
    'installment' => 1,
    'testMode' => true,
    'currency' => Nestpay\Currency::TRY,
]);
```

## Change log

Please see [UPGRADE](UPGRADE.md) for more information on how to upgrade to the latest version.

## Support

If you are having general issues with Payconn, we suggest posting on
[Stack Overflow](http://stackoverflow.com/). Be sure to add the

If you believe you have found a bug, please report it using the [GitHub issue tracker](https://github.com/payconn/nestpay/issues),
or better yet, fork the library and submit a pull request.


## Security

If you discover any security related issues, please email muratsac@mail.com instead of using the issue tracker.


## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

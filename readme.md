Yii2 FontAwesome Asset
======
Adding [FontAwesome](http://fontawesome.io/) to your Yii2 project via Composer

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```sh
php composer.phar require --prefer-dist sersid/yii2-font-awesome-asset "*"
```

or add

```
"sersid/yii2-font-awesome-asset": "*"
```

to the require section of your `composer.json` file.



Usage
-----

The following example is if you wish to register the bundle on a specific view

```php
// this code is written on that specific view
sersid\fontawesome\Asset::register($this);
```

But it could be that you wish to use it as part of another asset bundle or globally registered on your application. For the following example, we going to registered as part of the main application asset bundle AppAsset:

```php
class AppAsset extends AssetBundle
{
    public $depends = [
        ...
        'sersid\fontawesome\Asset'
    ];
}
```
# Curl Wrapper for Yii2 framework

## Requirements
* PHP 5.4+
* Yii 2.0.x
* Curl and php-curl installed

## Setup instructions

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).


```bash
php composer.phar require --prefer-dist peterfrench/yii2-curl "*"
```

Once composer installs the extension, include the component in your config file.

```php
	'curl' => [
		'class' => 'vendors\peterfrench\yii2-curl\Curl',
		'options' => [/* additional curl options */],
	],
```


## Usage
* to GET a page with default params

```php
	$output = Yii::$app->curl->get($url, $params);
	// output will contain the result of the query
	// $params - query that'll be appended to the url
```


* to POST data to a page

```php
	$output = Yii::$app->curl->post($url, $data);
	// $data - data that will be POSTed

```


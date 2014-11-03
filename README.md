laravel4
========

1. Environment

* Ubuntu 14.04.1 LTS

* Memory 4096MB

2. Setup

* installing for base

`~$ sudo apt-get update`

`~$ sudo apt-get install curl`

`~$ sudo apt-get install php5-cli `

`~$ sudo apt-get install mysql-server mysql-client`

`~$ sudo apt-get install php5-mysql`

* install composer with curl and php

`~$ sudo curl -sS https://getcomposer.org/installer | php` then we can use `php composer.phar install`

But, it should have `composer.json` file in same direcotry as this.

> {
>
>         "require": {
> 
>                 "dflydev/markdown": "1.0.3"
> 
>         }
>
> }
>

* if you want to upgrade (or update) to latest version, command `php composer.phar update`.
* downloaded packages are stored on directory `vendor` and we will use it as type `require 'vendor/autoload.php';`
* 

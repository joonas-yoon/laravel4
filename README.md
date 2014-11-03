laravel4
========

#### Environment

* Ubuntu 14.04.1 LTS

* Memory 4096MB

#### Setup

installing for base

```
~$ sudo apt-get update
~$ sudo apt-get install curl
~$ sudo apt-get install apache2
~$ sudo apt-get install php5-cli
~$ sudo apt-get install mysql-server mysql-client
~$ sudo apt-get install php5-mysql
```

install composer with curl and php

`~$ sudo curl -sS https://getcomposer.org/installer | php` then we can use `php composer.phar install`

But, it should have `composer.json` file in same direcotry as this.

```
{
    "require": {
        "dflydev/markdown": "1.0.3"
    }
}
````

if you want to upgrade (or update) to latest version, command `php composer.phar update`.

downloaded packages are stored on directory `vendor` and we will use it as type `require 'vendor/autoload.php';`

#### Start laravel

Using Laravel, read this: http://laravel.com/docs/4.2/quick

##### Setting

command `composer create-project laravel/laravel <project-name> --prefer-dist`.

Solution:

* Mcrypt PHP extension required ?

    : Type `php5enmod mcrypt` to enable and `php -i | grep mcrypt` for check mcrypt
     
* Error in exception handler ?

    : `chmod 777 <project-name>/app/storage/*`
    
* Does not working Router ?

    : make `AllowOverride` to `All` (from `None`) at apache configure file.

#### Reference URLs

writen down in korean.

* Laravel 4 - http://laravel.com/docs/4.2/quick
* APM setup - http://blog.lael.be/post/73
* Composer - http://opentutorials.org/course/62/5221
* Composer? - http://haruair.com/blog/1860

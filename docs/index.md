# Let's get Started

1. First install Composer to install Laravel.

`Why Composer and What is Composer?`


Composer is an application-level dependency manager for the PHP programming language that provides a standard format for managing dependencies of PHP software and required libraries. 

1. Go to the site `https://getcomposer.org/download/` and run following commands in your terminal.

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
1. You can see a file name `composer.phar` in your perent working Directory.

1. Most likely, you want to put the composer.phar into a directory on your PATH, so you can simply call composer from any directory (Global install).
```bash
sudo mv composer.phar /usr/local/bin/composer
```
1. To test your composer run following command.

```bash 
$ php composer
```
1. You will see Composer CLI.
1. Now you can create a new project of laravel.
1. change directory as following.
```bash
geek@g3:~$ cd /var/www/html/
geek@g3:/var/www/html$ 
```
1. Run following command to create your project name `blog`.
```bash
geek@g3:/var/www/html$ sudo composer create-project laravel/laravel blog
```
1. To check your app execute following command.
```bash
geek@g3:/var/www/html$ cd blog/
geek@g3:/var/www/html/blog$ ls
app        composer.json  database      phpunit.xml  resources  tests
artisan    composer.lock  lang          public       routes     vendor
bootstrap  config         package.json  README.md    storage    vite.config.js
geek@g3:/var/www/html/blog$ 
```
1. You have to set writeable permison to some directory.
```bash
geek@g3:/var/www/html/blog$ sudo chmod 777 -R bootstrap/cache/
geek@g3:/var/www/html/blog$ sudo chmod 777 -R storage/
``` 
1. Now to see welcome page of laravel at your localhost.
```bash
geek@g3:/var/www/html/blog$ php artisan serve
```
1. Now you will see the welcome page of Laravel.

Happy Laerning

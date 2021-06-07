# Install MS SQL PDO Driver on Multiple PHP Versions
Before digging into how to install MS SQL driver you should know how to switch between PHP versions correctly.

## Switching & Installing MS SQL driver for PHP 7.4 
### 1. Switching to PHP 7.4
```shell 
sudo update-alternatives --set php /usr/bin/php7.4
sudo update-alternatives --set phar /usr/bin/phar7.4
sudo update-alternatives --set phar.phar /usr/bin/phar.phar7.4
sudo update-alternatives --set phpize /usr/bin/phpize7.4
sudo update-alternatives --set php-config /usr/bin/php-config7.4
```
### 2. Install MS PDO SQL driver for PHP 7.4 
```shell
sudo pecl uninstall -r sqlsrv
sudo pecl uninstall -r pdo_sqlsrv
sudo pecl -d php_suffix=7.4 install sqlsrv
sudo pecl -d php_suffix=7.4 install pdo_sqlsrv
```
```shell
sudo su
printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/7.4/mods-available/sqlsrv.ini
printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/7.4/mods-available/pdo_sqlsrv.ini
exit
sudo phpenmod -v 7.4 sqlsrv pdo_sqlsrv
sudo service apache2 restart # or whatever your server or the PHP FPM. 
```
## Switching & Installing MS SQL driver for PHP 8.0
### 1. Switching to PHP 8.0
```shell
sudo update-alternatives --set php /usr/bin/php8.0
sudo update-alternatives --set phar /usr/bin/phar8.0
sudo update-alternatives --set phar.phar /usr/bin/phar.phar8.0
sudo update-alternatives --set phpize /usr/bin/phpize8.0
sudo update-alternatives --set php-config /usr/bin/php-config8.0
```

### 2. Install MS PDO SQL driver for PHP 8.0 
```shell
sudo pecl uninstall -r sqlsrv
sudo pecl uninstall -r pdo_sqlsrv
sudo pecl -d php_suffix=8.0 install sqlsrv
sudo pecl -d php_suffix=8.0 install pdo_sqlsrv
```
```shell
sudo su
printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/8.0/mods-available/sqlsrv.ini
printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/8.0/mods-available/pdo_sqlsrv.ini
exit
sudo phpenmod -v 8.0 sqlsrv pdo_sqlsrv
sudo service apache2 restart #or whatever your server or the PHP FPM. 
```

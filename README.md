# PHP_Test

### Тестовое задание:
```
Использовать Laravel
и любой шаблон сайта одностраничника , который что то продает , у которго есть кабинет для пользователя,
регистрация и прочее на внешней части сайта можно создать заявку на покупку продукта,
если не зарега - предлагается зарегестрироваться и продолжть покупку товара. товар добавляется
в виртуальную корзину, и то что в ней лежит можно просмотреть в личном кабинете. что бы купить что то
пользователь  должен пополнить баланс. списание будет идти с баланса (реальную работу пополнения
можно не делать, но нужно дедать лог пополнения) есть консольный скрипт, который запускается
1 раз в полночь и считает добавленые пользователем покупки в корзину и купленные пользователем
товары (просто количество добавленных товаров и количество купленных) и сохраняет в файл с датой
за котрую был совершен подсчет товар может быть один - это не суть важно

Для пользователя есть класс хелпер, котрый реализован через контракт, и в которм часто
сгруппированы частые функции, для работы с пользователем.
дизайн совершенно не важен - важна работа php
```


#### _Технологии_
> 1. PHP Version 7.2.8 
> 2. Laravel Version 
> 3. MySQL Ver 15.1 Distrib 10.1.33-MariaDB для хранения данных


## Для запуска программы: 

1. ```$ cp .env.example .env```
2. ```$ php artisan key:generate```
3. ```$ php artisan migrate```
4. ```$ php artisan passport:install```
5. ```$ php artisan db:seed```
6. ```$ npm install```
7. ```$ php artisan serve```


### или

#### Для Windows
> * [Загружать XAMPP PHP 7.2.8](https://www.apachefriends.org/xampp-files/7.2.8/xampp-win32-7.2.8-0-VC15-installer.exe) и установите
> * Перейти к `C:\\xampp\htdocs\` и клонировать из репозитория github `git clone https://github.com/Janik-Tarverdyan/store.tst.git`
> * Теперь необходимо создать виртуальный хост на локальном сервере XAMPP. 
Для этого нужно найти файл по имени `httpd-vhosts.conf` в XAMPP, расположение файла здесь `C:\\xampp\apache\extra\httpd-vhosts.conf` и добавить конфигурацию хоста в файл

### конфигурация хоста 
```
# store.tst
<VirtualHost store.tst:80>
  DocumentRoot "C:\\xampp\htdocs\store.tst\public\"
  ServerName store.tst
  ServerAlias www.store.tst
  ErrorLog "/var/log/httpd/www.store.tst-error_log"
  CustomLog "/var/log/httpd/store.tst-access_log" common
</VirtualHost>
```
> * После настройки хоста нужно добавить IP хоста для windows server в файл hosts его путь находится в 
    `C:\\Windows\System32\Drivers\etc\hosts` откройте файл и добавьте в файл эту строку, 
    если не существует `127.1.2.3 registration.tst`
    
     Перезапускайте XAMPP


___

#### Для Linux
> * [Загружать XAMPP PHP 7.2.5](https://www.apachefriends.org/xampp-files/7.2.5/xampp-linux-x64-7.2.5-0-installer.run) и установите
> * Перейти к `$PATH/xampp/htdocs/` и клонировать из репозитория github `git clone https://github.com/Janik-Tarverdyan/PHP_Test.git`
> * Теперь необходимо создать виртуальный хост на локальном сервере XAMPP.
    Для этого нужно найти файл по имени `httpd-vhosts.conf` в XAMPP,
    расположение файла здесь `$PATH/xampp/apache/extra/httpd-vhosts.conf` и добавить конфигурацию хоста в файл
>
### конфигурация хоста 
```
# store.tst
<VirtualHost store.tstt:80>
  DocumentRoot "$PATH/xampp/htdocs/store.tst/public/"
  ServerName store.tst
  ServerAlias www.store.tst
  ErrorLog "/var/log/httpd/www.store.tst-error_log"
  CustomLog "/var/log/httpd/store.tst-access_log" common
</VirtualHost>
```
> * После настройки хоста нужно добавить IP хоста в файл hosts его путь находится в 
    `/etc/hosts` откройте файл и добавьте в файл эту строку, 
    если не существует `127.1.2.3 store.tst`

    Перезапускайте XAMPP


## Рекомендации
>**Рекомендую использовать Firefox браузер, это самый лучший браузер для разработчиков и тестировщиков.**

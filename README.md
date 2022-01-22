Symfony Demo Application
========================

The "Symfony Demo Application" is a reference application created to show how
to develop applications following the **Symfony Best Practices**.

Requirements
------------

  * PHP 7.3 or higher;
  * PDO-SQLite PHP extension enabled;
  * and the usual Symfony application requirements.

Installation
------------

Install the `symfony` Vendor on your computer:

```bash
composer require symfony/runtime
composer install
```

Generate database, set rights and load fixtures
```bash
symfony console d:d:c
symfony console d:s:u —force

chown -R root:www-data ../demo
chmod -R 775 var 

php bin/console doctrine:fixtures:load
```

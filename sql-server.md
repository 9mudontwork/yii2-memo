# ต่อ SQL Server กับ Yii

โหลด driver .dll

{% embed url="https://docs.microsoft.com/en-us/sql/connect/php/system-requirements-for-the-php-sql-driver" %}

หลังจากนั้นแก้ php.ini

```php
extension=php_sqlsrv_73_ts_x64
extension=php_pdo_sqlsrv_73_ts_x64.dll
```

วิธี config connection

```php
'dsn' => 'sqlsrv:Server=localhost;Database=CUARDB',
```


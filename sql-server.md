# ต่อ SQL Server กับ Yii

## โหลด driver .dll

{% embed url="https://docs.microsoft.com/en-us/sql/connect/php/system-requirements-for-the-php-sql-driver" %}

## หลังจากนั้นแก้ php.ini

```php
extension=php_sqlsrv_73_ts_x64
extension=php_pdo_sqlsrv_73_ts_x64.dll
```

## วิธี config connection

```php
'dsn' => 'sqlsrv:Server=localhost;Database=INNOC_DB',
'username' => 'admin',
'password' => '',
```

## ตั้งค่า login

![](.gitbook/assets/image%20%284%29.png)

## ถ้าติด TCP/IP

![](.gitbook/assets/image%20%285%29.png)

## ทำให้เครื่องอื่น connect sql server ได้

{% embed url="https://naiwaen.debuggingsoft.com/2018/03/how-to-enable-remote-connections-in-microsoft-sql-server/" %}

## ถ้าหาก sql config ไม่เจอ

`SQLServerManager15.msc` สำหรับ \[SQL Server 2019\] หรือ

`SQLServerManager14.msc` สำหรับ \[SQL Server 2017\] หรือ

`SQLServerManager13.msc` สำหรับ \[SQL Server 2016\] หรือ

`SQLServerManager12.msc` สำหรับ \[SQL Server 2014\] หรือ

`SQLServerManager11.msc` สำหรับ \[SQL Server 2012\] หรือ

`SQLServerManager10.msc`สำหรับ \[SQL Server 2008\]


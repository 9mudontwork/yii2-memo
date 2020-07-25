# ติดตั้ง RBAC Manager

{% embed url="https://github.com/mdmsoft/yii2-admin" %}

ไปที่ 

```text
common\config\main.php
```

ใส่

```php
'aliases' => [
    '@mdm/admin' => '@vendor/mdmsoft/yii2-admin',
],
```

ไปที่

```php
backend\config\main.php
```

ใส่

```php
'modules' => [
    'admin' => [
        'class' => 'mdm\admin\Module',
    ]
],

'components' => [
    'authManager' => [
        'class' => 'yii\rbac\PhpManager', // or use 'yii\rbac\DbManager'
    ]
],

'as access' => [
    'class' => 'mdm\admin\components\AccessControl',
    'allowActions' => [
        'site/*',
        'admin/*',
        'some-controller/some-action',
    ]
],
```






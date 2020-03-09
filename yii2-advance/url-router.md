# ตั้งค่า Url Router

## ที่อยู่ไฟล์

```text
frontend\config\main.php
backend\config\main.php
```

## กำหนดค่า

```php
'urlManager' => [
    'enablePrettyUrl' => true,
    'showScriptName' => false,
    'rules' => [
        '<module:\w+>/<controller:\w+>/<id:\d+>' => '<module>/<controller>/view',
        '<module:\w+>/<controller:\w+>/<action:\w+>/<id:\d+>' => '<module>/<controller>/<action>',
        '<module:\w+>/<controller:\w+>/<action:\w+>' => '<module>/<controller>/<action>',

        '<controller:\w+>/<id:\d+>' => '<controller>/view',
        '<controller:\w+>/<action:\w+>/<id:\d+>' => '<controller>/<action>',
        '<controller:\w+>/<action:\w+>' => '<controller>/<action>',
    ],
],
```


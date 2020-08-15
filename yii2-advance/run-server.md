# การติดตั้ง และ run server

## Document

{% embed url="https://www.yiiframework.com/extension/yiisoft/yii2-app-advanced/doc/guide/2.0/en/start-installation" %}

## ติดตั้ง

```text
composer global require fxp/composer-asset-plugin
composer create-project --prefer-dist yiisoft/yii2-app-advanced .

composer install
composer dumpautoload
php init
```

## run server

```text
php yii serve --docroot="frontend\web" --port=8080

php yii serve --docroot="backend\web" --port=8081
```

## ตั้งค่าการเชื่อมต่อฐานข้อมูล

```text
common\config\main-local.php
```


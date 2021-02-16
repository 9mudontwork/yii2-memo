# สร้าง Class ใช้งานเอง

สร้างไฟล์ที่

```text
frontend\components
```

register component ที่

```text
frontend\config\main.php
```

```php
'components' => [
        //....
        'meta' => [
            'class' => 'frontend\components\MetaComponent',
        ],
        //....
],
```

เรียกใช้งาน method ของ class ที่สร้างขึ้นเองที่ หรือ ไฟล์ layout ของ theme

```php
frontend\views\layouts\main.php
```

```php
<?php Yii::$app->meta->displaySeo() ?>
```

กำหนดค่าแต่ละหน้าใน view

```php
Yii::$app->meta->keywords = 'programmer,thailand,seo,search engine';
```


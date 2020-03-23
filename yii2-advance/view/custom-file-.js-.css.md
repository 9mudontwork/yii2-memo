# Custom File .js .css

{% embed url="http://dixonsatit.github.io/2015/06/20/disable-bootstrap-js-css-jquery.html" %}

{% embed url="http://dixonsatit.github.io/2015/06/23/client-script.html" %}



ตัวอย่าง

```php
//
frontend\config\main.php

return [
    // ...
    'components' => [
        'assetManager' => [
            'bundles' => [
                'yii\web\JqueryAsset' => [
                'sourcePath' => null,
                'basePath' => '@webroot',
                'baseUrl' => '@web',
                'js' => [
                        'jquery.min.js',
                    ]
                ],
            ],
        ],
    ],
];

//-------------------

return [
    // ...
    'components' => [
        'assetManager' => [
            'bundles' => [
                'yii\web\JqueryAsset' => [
                    'sourcePath' => null,
                    'js' => [
                        '//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js',
                    ]
                ],
            ],
        ],
    ],
];
```

เข้าไปแก้ไขไฟล์ที่

```text
backend\web
```

แล้วก็เพิ่ม path ไฟล์ที่

```text
backend\assets\AppAsset.php
```

ถ้าต้องการปิด asset ที่ yii เตรียมไว้ให้

```php
'assetManager' => [
    'bundles' => [
        'yii\web\YiiAsset' => false,
        'yii\bootstrap4\BootstrapAsset' => false,
    ],
],
```

ถ้าต้องการ register ไฟล์ js ของเราให้อยู่ข้างล่าง asset ของ yii

```php
$this->registerJsFile('@web/js/step4.js', ['depends' => 'frontend\assets\AppAsset', 'position' => View::POS_HEAD]);
```

css

```php
$this->registerCssFile("@web/css/css.css", ['depends' => 'frontend\assets\AppAsset']);
```

ตั้งค่า depend ที่ AppAsset

```php
'yii\web\YiiAsset',
'yii\widgets\ActiveFormAsset',
'yii\widgets\PjaxAsset',
'yii\grid\GridViewAsset',
'yii\bootstrap4\BootstrapAsset',
'yii\bootstrap4\BootstrapPluginAsset',
```


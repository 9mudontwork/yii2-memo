# Krajee yii2-widget-fileinput

## Krajee yii2-widget-fileinput

{% embed url="https://github.com/kartik-v/yii2-widget-fileinput" %}

## การติดตั้ง

```text
composer require kartik-v/yii2-widget-fileinput "@dev"
```

## การตั้งค่า

ตั้งค่าเพื่อเลือกใช้ Bootstrap 3 หรือ 4

frontend\config\params.php

```text
'params' => [
    'bsVersion' => '4.x', // or 3.x
]
```

## การใช้งาน

### import

```php
use kartik\file\FileInput;
```

### ตัวอย่างการใช้งาน

```php
// Usage with ActiveForm and model
echo $form->field($model, 'avatar')->widget(FileInput::classname(), [
    'options' => ['accept' => 'image/*'],
]);
 
// With model & without ActiveForm
echo '<label class="control-label">Add Attachments</label>';
echo FileInput::widget([
    'model' => $model,
    'attribute' => 'attachment_1[]',
    'options' => ['multiple' => true]
]);
 
// Usage without a model
echo '<label class="control-label">Upload Document</label>';
echo FileInput::widget([
    'name' => 'attachment_3',
]);
 
// A disabled fileinput input
echo '<label class="control-label">Select Attachment</label>';
echo FileInput::widget([
    'name' => 'attachment_4',
    'disabled' => true
]);
```

### ตัวอย่างอื่น ๆ

{% embed url="https://demos.krajee.com/widget-details/fileinput" %}

{% embed url="https://plugins.krajee.com/file-input/demo" %}


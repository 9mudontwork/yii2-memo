# Input Form

## Active Form

```php
<?php
$form = ActiveForm::begin([
    'id' => 'area_map_form',
    'options' => ['enctype' => 'multipart/form-data'],
    // 'enableClientValidation' => true
]);
?>

<?php ActiveForm::end(); ?>
```

## Dropdown List

```php
echo $form->field($model->building, 'id')->dropDownList(ArrayHelper::map($data->buildingList, 'id', 'name'), [
    'options' => [
        'id' => 'area_building_id',
        'placeholder' => 'เลือกอาคาร'
    ],
])->label(false);
```


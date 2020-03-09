# dependent DropdownList

## FORM

```php
$webboardRoom = WebboardRoom::find()->select(['id', 'name'])->where(['webboard_category_id' => $model->webboard_category_id])->asArray()->all();


<?php
$webboardCategoryList = [
    1 => 'จัดการห้ององค์ความรู้',
    2 => 'จัดการห้องไลฟ์สไตล์/เรื่องทั่วไป',
];
?>

<?= $form->field($model, 'webboard_category_id')->dropDownList($webboardCategoryList, ['id' => 'webboard-category-id']) ?>

<?php

echo $form->field($model, 'webboard_room_id')->widget(DepDrop::classname(), [
    'data' => ArrayHelper::map($webboardRoom, 'id', 'name'),
    'pluginOptions' => [
        'depends' => ['webboard-category-id'],
        'placeholder' => 'เลือก...',
        'url' => Url::to(['/webboard/webboard-room/'])
    ]
]);

?>
```

## Controller

```php
public function actionWebboardRoom()
{
    Yii::$app->response->format = \yii\web\Response::FORMAT_JSON;
    $out = [];
    if (isset($_POST['depdrop_parents'])) {
        $parents = $_POST['depdrop_parents'];
        if ($parents != null) {
            $webboardCategoryId = $parents[0];
            $out = self::getWebboardRoomByCategory($webboardCategoryId);
            return ['output' => $out, 'selected' => ''];
        }
    }
    return ['output' => '', 'selected' => ''];
}

public function getWebboardRoomByCategory($categoryId)
{
    $model = new WebboardRoom();
    return $model->find()->select(['id', 'name'])->where(['webboard_category_id' => $categoryId])->asArray()->all();
}
```


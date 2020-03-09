# Update

## Custom Method

```php
protected function findOneRowByModel($id ,$model)
{
    if (($model = $model::findOne($id)) !== null) {
        return $model;
    }

    throw new NotFoundHttpException('The requested page does not exist.');
}
```

## ถ้า Field ตรงกันกับ Model

```php
/**
 * ===== Muhammad Imoeb =====
 */
 
$model = $this->findOneByModel($id, 'nameModel');

// ถ้ามี Post ที่ผูกกับ Model ส่งมา
if ($model->load(Yii::$app->request->post())) {

    // รับค่าจาก POST มาเก็บ
    $postData = Yii::$app->request->post();

    // เริ่มตรวจสอบการ query
    $transaction = Yii::$app->db->beginTransaction();

    /** ===== Logic ===== */
    /** ===== End Login ===== */

    // ลองบันทึก
    // ถ้าผ่านให้ query
    // ถ้าไม่ผ่าน โยน Excenption และไม่ query
    try {
        if ($model->save()) {
            $transaction->commit();
            return $this->redirect(['view', 'id' => $model->id]);
        }
    } catch (\Exception $e) {
        $transaction->rollBack();
    }

    // render view
    return $this->render('update', [
        'model' => $model,
    ]);
}
```

## ถ้า Field ไม่ตรงกับ Model

```php
/**
 * ===== Muhammad Imoeb =====
 */
 
$model = $this->findOneByModel($id, 'nameModel');

// ถ้ามี Post ที่ผูกดับ Model ส่งมา
if ($model->load(Yii::$app->request->post())) {

    // รับค่าจาก POST มาเก็บ
    $postData = Yii::$app->request->post();

    // เริ่มตรวจสอบการ query
    $transaction = Yii::$app->db->beginTransaction();

    /** ===== Logic ===== */
    Console::Table($model->attributes);

    // เซ็ตข้อมูลใส่ field model
    $model->name = $postData['name'];
    /** ===== End Login ===== */

    // ลองบันทึก
    // ถ้าผ่านให้ query
    // ถ้าไม่ผ่าน โยน Excenption และไม่ query
    try {
        if ($model->save()) {
            $transaction->commit();
            return $this->redirect(['view', 'id' => $model->id]);
        }
    } catch (\Exception $e) {
        $transaction->rollBack();
    }

    // render view
    return $this->render('update', [
        'model' => $model,
    ]);
}
```


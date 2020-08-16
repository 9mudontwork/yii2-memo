# Utils Function สำหรับ Yii

```php
<?php

namespace frontend\components;

use Yii;
use DateTime;
use yii\helpers\Url;

class Utils
{
    /** =============== Utils Function =============== */
    public static function currentDateTime()
    {
        $dateTime = new DateTime();
        return $dateTime->format('Y-m-d H:i:s');
    }

    public static function formatDMYtoYMD($date)
    {
        $date = new DateTime($date);
        return $date->format('Y-m-d');
    }

    public static function formatYMDtoDMY($date)
    {
        $date = new DateTime($date);
        return $date->format('d-m-Y');
    }

    public static function isset($value)
    {
        if (isset($value) && !empty($value)) {
            return true;
        }

        return false;
    }
    /** =============== End Utils Function =============== */





    /** =============== DEBUG Function =============== */
    public static function debug($data)
    {
        \Yii::debug($data);
    }

    public static function debugAttributes($model)
    {
        if ($model)
            \Yii::debug(['ตาราง' => $model->tableName(), 'ค่าในฟิล' => $model->attributes]);
    }

    public static function debugValidateModel($model)
    {
        if ($model) {
            \Yii::debug(['ตาราง' => $model->tableName(), 'ค่าในฟิล' => $model->attributes]);
            $model->validate();
            \Yii::debug(['ตาราง' => $model->tableName(), 'ฟิลที่ error' => $model->getErrors()]);
        }
    }
    /** =============== END DEBUG Function =============== */





    /** =============== Manage Model Function =============== */
    public static function saveModel($model)
    {
        return $model->save() ? true : self::debugValidateModel($model);
    }

    public static function saveAllModel(array $models)
    {
        $save = function ($model) {
            return $model->save() ? true : self::debugValidateModel($model);
        };

        foreach ($models as $model) {
            if (!$save($model)) {
                return false;
            }
        }

        return true;
    }

    public static function setupModel($model, array $data)
    {
        if (self::isset($data)) {
            foreach ($data as $key => $value) {
                $model->$key = $value;
            }
        }

        return $model;
    }
    /** =============== End Manage Model Function =============== */




    /** =============== Yii Utils Function =============== */
    public static function isUserGoHome()
    {
        if (!Yii::$app->user->isGuest) {
            return Yii::$app->getResponse()->redirect(Url::home());
        }
    }

    public static function isGuestGoHome()
    {
        if (Yii::$app->user->isGuest) {
            return Yii::$app->getResponse()->redirect(Url::home());
        }
    }

    public static function currentUserId()
    {
        return Yii::$app->user->getId();
    }

    public static function isThaiLanguage()
    {
        return Yii::$app->language == 'th' ? true : false;
    }

    public static function currentLanguage()
    {
        return Yii::$app->language;
    }
    /** =============== End Utils Function =============== */
}

```


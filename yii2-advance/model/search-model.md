# Custom Search & Gridview

{% embed url="https://github.com/jacksontong/Yii2-gridview-example" %}

## ตัวอย่างชั่วคราว

```php
$query = Users::find()
            ->leftjoin('profile', 'profile.user_id = user.id')
            ->leftjoin('department', 'department.id = profile.department_id')
            ->where([
                'user.role_id' => '5'
            ]);
            
            
->andFilterWhere(['like', 'department.short_department', $this->department_id])
```


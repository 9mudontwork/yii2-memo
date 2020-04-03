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

```php
$query = LogUser::find()
            ->select([
                'log_user.*',

                'user.username as user__username',
                'user.role_id as user__role_id',

                'role.id as role__id',
                'role.role as role__name'
            ])
            ->leftJoin('user', 'user.id = log_user.user_id')
            ->leftJoin('role', 'role.id = user.role_id')
            ->where('role.role = "ผู้ดูแลระบบ"');
            
            
$dataProvider = new ActiveDataProvider([
            'query' => $query,
            'key' => 'id',
            'sort' => [
                'attributes' => [
                    'user__username',
                ],
                'defaultOrder' => [
                    // 'id' => SORT_ASC,
                ]
            ]
        ]);
```




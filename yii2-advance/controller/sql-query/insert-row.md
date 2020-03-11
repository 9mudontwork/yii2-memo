# Insert หลายๆ row พร้อมกัน

```php
$projectDocumentFile = [];
                foreach ($fileUpload as $file) {
                    $projectDocumentFile[] = [
                        'project_document_id' => $model->id,
                        'file_name' => $file['name'],
                        'file_code' => json_encode($file),
                        'file_key' => $file['key'],
                        'created_at' => date("Y-m-d H:i:s"),
                        'updated_at' => date("Y-m-d H:i:s"),
                    ];
                }
                $projectDocumentFileField = [
                    'project_document_id',
                    'file_name',
                    'file_code',
                    'file_key',
                    'created_at',
                    'updated_at',
                ];
                Yii::$app->db
                    ->createCommand()
                    ->batchInsert(ProjectDocumentFile::tableName(), $projectDocumentFileField, $projectDocumentFile)
                    ->execute();
```


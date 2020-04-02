# ตัวอย่าง Validate Rule ใน Model

```php
[
['thumbnail_video'], 'required', 'message' => '{attribute} ต้องไม่ว่าง',
'whenClient' => "function (attribute, value) {
                return $('#multimedia-type').val() == 'video';
            }"
],
[
['url_youtube'], 'required', 'message' => '{attribute} ต้องไม่ว่าง',
'whenClient' => "function (attribute, value) {
                return ($('#upload-type').val() == 'youtube' && $('#multimedia-type').val() == 'video');
            }"
],
```




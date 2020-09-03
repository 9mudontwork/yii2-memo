# Run Local Server

```text
composer global require fxp/composer-asset-plugin
composer create-project --prefer-dist yiisoft/yii2-app-advanced .

composer install
composer dumpautoload
php init
```

## run yii server

```text
php yii serve --docroot="frontend\web" --port=8080

php yii serve --docroot="backend\web" --port=8081
```

## Run Sass

```text
ถ้ายังไม่มี sass ติดตั้ง sass ก่อน
npm install -g sass 

run command

##### fontend #####
(compile css file)
sass --watch frontend/web/sass/custom-style.scss:frontend/web/css/custom-style.css

(compile min.css file)
sass --watch --style=compressed frontend/web/sass/custom-style.scss:frontend/web/css/custom-style.css


##### backend #####
(compile css file)
sass --watch backend/web/sass/custom-style.scss:backend/web/css/custom-style.css

(compile min.css file)
sass --watch --style=compressed backend/web/sass/custom-style.scss:backend/web/css/custom-style.css

** ไม่ push ไฟล์ 
.css 
.css.map
```




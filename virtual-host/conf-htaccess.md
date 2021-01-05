# ตั้ง conf หรือ htaccess

## htaccess



_Finally I made it working:-_

_**1.**_ _created two .htaccess file \(one on root and one in web folder of my application\):-_

_root .htaccess:-_

```text
<IfModule mod_rewrite.c>
    Options +FollowSymlinks
    RewriteEngine On
</IfModule>

<IfModule mod_rewrite.c>
    RewriteCond %{REQUEST_URI} ^/.*
    RewriteRule ^(.*)$ web/$1 [L]

    RewriteCond %{REQUEST_URI} !^/web/
    RewriteCond %{REQUEST_FILENAME} !-f [OR]
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^.*$ web/index.php
</IfModule> 
```

_web folder .htaccess:-_

```text
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . index.php
```

_**2.**_ _In config/web.php:-_

```text
'urlManager' => [
        'enablePrettyUrl' => true,
        'showScriptName' => false,
        'rules' => [
        // Your rules here
        ],
    ],
```

_**3.**_ _Changed in \(apache2.conf\) like below:-_

```text
<Directory /var/www/html/>
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>
```

## Conf

```text
<VirtualHost *:80>
    ServerName example.com
    ServerAdmin admin@example.com

    DocumentRoot /var/www/example.com/html/frontend/web
    <Directory /var/www/example.com/html/frontend/web>
        Options FollowSymLinks
        AllowOverride None
        Require all granted

        RewriteEngine on
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteRule . index.php
    </Directory>

    ErrorLog  ${APACHE_LOG_DIR}/example.com.frontend.error.log
    CustomLog ${APACHE_LOG_DIR}/example.com.frontend.access.log combined
</VirtualHost>
```

```text
<VirtualHost *:80> 
    DocumentRoot "C:/Users/i3acksp4ce/Desktop/INNOC/frontend/web/"
    ServerName f.innoc.test
    ServerAlias *.f.innoc.test
    <Directory "C:/Users/i3acksp4ce/Desktop/INNOC/frontend/web/">
        AllowOverride All
        Require all granted

        RewriteEngine on
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteRule . index.php
    </Directory>
</VirtualHost>

# If you want to use SSL, enable it by going to Menu > Apache > SSL > Enabled

```


注意伪静态 .htaccess修改

```
<IfModule mod_rewrite.c>
Options +FollowSymlinks
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.*)$ index.php?/$1 [QSA,PT,L]
</IfModule>
```




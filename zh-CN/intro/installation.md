---
name: 下载安装
---

### 下载

请在下载页面查看最新版本 https://github.com/orvice/ss-panel/releases

这里以ss-panel下载至`/home/www/ss-panel`目录为例


```
cd /home/www
git clone https://github.com/orvice/ss-panel.git 
```

### 服务器配置  


#### Apache设置

VirtualHost配置中增加

```
<Directory /home/www/ss-panel/public>
   AllowOverride All
   Order Deny,Allow
   Allow from all
</Directory>
```

并且需要开启`mod_rewrite`模块。

#### Nginx设置

```
root /home/www/ss-panel/public;

location / {
   try_files $uri $uri/ /index.php$is_args$args;
}    
```


### 基本配置

#### 导入数据库

将db.sql导入数据库中。

#### 设置权限

确保storage有读写权限:

```
chmod -R 777 storage
```

#### 复制一份配置文件

```
cp .env.example .env
```

#### 

#### 使用composer安装第三方库

```
cd /home/www/ss-panel
curl -sS https://getcomposer.org/installer | php
php composer.phar  install
```

如果出现错误，请按照错误信息安装相应的php模块，然后再执行 `php composer.phar  install`


到此，ss-panel安装完毕，请继续阅读配置。



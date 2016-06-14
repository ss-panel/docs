---
name: 配置
---


## 配置

ss-panel v3 配置说明，请根据说明合理选择密码加密方式，认证方式等。

修改站点以及数据库配置
```
vim .env
```

### Auth Driver 认证设置

ss-panel v3支持多种存储用户认证信息的方式：

* file 使用文件存储sessions。 
* redis 使用Redis存储，推荐此方式。

推荐使用redis

#### 安装Redis
```
apt-get install redis-server
```

### 密码加密方式

* md5 不推荐
* sha256 推荐

### 添加管理员

在网站根目录下执行

```
php xcat createAdmin
```

根据提示创建管理员帐号。

创建成功后登录可以在/admin进行管理。

### 重置流量

```
php xcat resetTraffic
```


### 发送流量使用情况邮件

```
php xcat sendDiaryMail
```

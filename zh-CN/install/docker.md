---
name: 使用Docker安装
---

### 安装Docker

```
apt-get install \
     apt-transport-https \
     ca-certificates \
     curl \
     software-properties-common

curl -fsSL https://download.docker.com/linux/debian/gpg |  apt-key add -

add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
   
apt-get update
apt-get install docker-ce
```

### 安装docker-compose

```
curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose 
chmod +x  /usr/local/bin/docker-compose 

```


###  安装ss-panel

```
mkdir /ss-panel
cd /ss-panel
wget https://raw.githubusercontent.com/orvice/ss-panel/master/docker-compose.yml
docker-compose up -d
```
 
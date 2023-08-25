---
{"dg-publish":true,"aliases":null,"tags":["图床","兰空","docker"],"title":"群晖docker安装开源图床Lsky Pro","permalink":"/0102/docker/docker-lsky-pro/","dgPassFrontmatter":true,"noteIcon":""}
---


> GitHub 上有小伙伴说通过群晖的 Docker 安装 Lsky Pro 图床失败，自己试了一下，没有发现什么问题，整理一下操作步骤，给需要的小伙伴作参考！

## 写在前面

Lsky Pro 图床程序支持多种数据库类型，如常见的 MySQL/SQLite 等，该文以 SQLite 为例，截图在群晖 Docker 上的部署过程。

我的群晖型号为 DS918+，系统版本为 DSM 7.1-42661 Update 1，Docker 套件的版本为 20.10.3-1306。

## 操作步骤

### 首先进入 Docker 注册表，搜索关键词 `HalcyonAzure/lsky-pro-docker`，出现的结果中，直接下载：



![img](https://552210.xyz:1002/i/2023/04/27/64496a80bc6d1.webp)



### 映像约 836M ，下载好后启动。网络默认的 bridge 即可：



![img](https://552210.xyz:1002/i/2023/04/27/64496a80bc6d1.webp)



### 下一步后，记得勾选启用自动重新启动：



![img](https://552210.xyz:1002/i/2023/04/27/64496a80a7465.webp)



### 下一步，设置访问端口，如不设置，也可使用自动生成端口，对图床使用无影响：



![img](https://552210.xyz:1002/i/2023/04/27/64496a80bc6d1.webp)



### 下一步，设置目录映射，添加文件夹，将群晖本地文件夹`/docker/lsky`映射到 `/var/www/html`，最后确认完成：



![img](https://552210.xyz:1002/i/2023/04/27/64496a80b15e0.webp)



### 通过浏览器打开该容器访问地址`http://域名:1180`,在设置数据库时选择 SQLite 就可以了（此处的数据库名称/路径不填）

### 最后注意分享的照片地址可能是内网地址时，注意以下界面的设置.



![img](https://552210.xyz:1002/i/2023/04/27/64496a80a3c1a.webp)

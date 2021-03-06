# 参数

Phabricator 预装包包含 Phabricator 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

### Phabricator

Phabricator 安装目录： */data/wwwroot/phabricator*  
Phabricator 配置文件： */data/wwwroot/phabricator/phabricator/conf/local/local.json*  

> Phabricator 配置文件数据库连接信息，更改了 MySQL 数据库账号密码，此处也需要对应修改

### PHP

PHP 配置文件: */etc/php/7.2/apache2/php.ini*

### Apache

Apache 虚拟主机配置文件：*/etc/apache2/sites-enabled/000-default.conf*  
Apache 主配置文件： */etc/apache2/apache2.conf*  
Apache 日志文件： */var/log/apache2*

### MYSQL

MySQL 安装路径: */usr/share/mysql*  
MySQL 数据文件 */data/mysql*  
MySQL 配置文件: */etc/mysql/my.cnf*    
MySQL 可视化管理地址: *http://服务器公网IP:9090*，用户名和密码请见 [账号密码](/zh/stack-accounts.md) 章节。


## 端口号

下面是您在使用本镜像过程中，需要用到的端口号，请通过 [云控制台安全组](https://support.websoft9.com/docs/faq/zh/tech-instance.html)进行设置

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| HTTP | 80 | 通过http访问Phabricator | 必须 |
| HTTPS | 443 | 通过https访问Phabricator | 可选 |
| MySQL | 3306 | 远程连接MySQL | 可选 |
| phpMyAdmin on Docker | 9090 | 可视化管理MySQL | 可选 |

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# PHP Version
php -v

# Apache version:
apache2 -v

# MySQL version:
mysql -V

# Dokcer:
docker --version
```
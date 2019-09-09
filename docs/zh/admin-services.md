# 服务启停

使用由Websoft9提供的Phabricator部署方案，可能需要用到的服务如下：

### Phabricator

```shell
sudo systemctl start metabase
sudo systemctl stop metabase
sudo systemctl restart metabase
sudo systemctl status metabase
```

### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

### MySQL

```shell
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql
sudo systemctl status mysql
```


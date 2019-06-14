# Mysql


##安装mysql

####环境 centos 6.8 64位
 
安装 
> `yum install mysql-server -y`

启动服务
>`service mysqld restart`

为root设置密码
>`/usr/bin/mysqladmin -u root password 'root'`

登录MySQL数据库
>`mysql -u root -p`

MySQL中使用下列命令
>`use mysql`

>`grant all privileges on *.* to 'root'@'%' identified by 'root' ;`

>`flush privileges;`


# docker
docker pull mysql

![](http://pic.wmgblog.pw/20190321214640.png)

设置 
docker run --name mysql  -p 3307:3306 -e MYSQL_ROOT_PASSWORD=root

## 然后进入mysql容器 命令行

> docker exec -it mysql bash 

> mysql -u root -p

> `grant all privileges on *.*  to 'root'@'%' ; `

> flush privileges; 

### 如果 远程 链接 出错

mysql 8.0 默认使用 caching_sha2_password 身份验证机制 —— 从原来的 mysql_native_password 更改为 caching_sha2_password

Mysql远程连接报错：authentication plugin caching_sha2

> ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';

(参考链接1)[https://blog.csdn.net/gf0515/article/details/80466213]

# Windows

> mysqld.exe --install
> mysql -uroot -proot

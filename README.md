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



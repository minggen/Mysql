
##��װmysql

####���� centos 6.8 64λ
 
��װ 
> `yum install mysql-server -y`

��������
>`service mysqld restart`

Ϊroot��������
>`/usr/bin/mysqladmin -u root password 'root'`

��¼MySQL���ݿ�
>`mysql -u root -p`

MySQL��ʹ����������
>`use mysql`

>`grant all privileges on *.* to 'root'@'%' identified by 'root' ;`

>`flush privileges;`



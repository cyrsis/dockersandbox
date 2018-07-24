[root@bfd-v7 ~]# docker run --name test-mysql -p 3308:3306  -e MYSQL_ROOT_PASSWORD=123456 -d mysql

#进入mysql的终端
[root@bfd-v7 ~]# docker exec -it test-mysql mysql -uroot -p123456

##Windows
`docker run --name mysql01 -d -p 3306:3306 mysql/mysql-server:5.7.21 --character-set-server=utf8mb4 --collation-server=utf8mb4_general_ci`

`docker exec -it mysql01 bash`

Get the password from the log file

`mysql –uroot -p`

Change Password

`ALTER USER 'root'@'localhost' IDENTIFIED BY 'abc123456';`

Create new user to access
`CREATE USER 'abc'@'%' IDENTIFIED BY 'abc123456' require none;`

Confirm

`select user,host from user;`

`GRANT ALL PRIVILEGES ON *.* TO 'abc'@'%' WITH GRANT OPTION;`

Login with abc:abc123456


--Linux
docker run -p 3306:3306 --name mymysql -v $PWD/mysql/logs:/logs -v $PWD/mysql/data:/mysql_data -e MYSQL_ROOT_PASSWORD=123456 -d mysql:latest sleep infinity


Exit
`exit;`

### 进入之后，要对用户进行授权，否则用navicat连接不上。
GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' IDENTIFIED BY '123456';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'192.168.12.5' IDENTIFIED BY '123456';
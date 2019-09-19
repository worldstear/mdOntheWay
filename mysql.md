## mysql相关
```
use mysql;
select host,user from user;
```
### 创建用户
```
create user 'username@%' identified by 'password';
```
### 赋予权限
```
grant all privileges on mysql_db.* to 'username'@'';
```
### 修改加密协议(解决远程登录时候协议问题)
```
alter user 'root'@'localhost' identified with mysql_native_password by 'password';
```
### 刷新权限
```
flush privileges;
```

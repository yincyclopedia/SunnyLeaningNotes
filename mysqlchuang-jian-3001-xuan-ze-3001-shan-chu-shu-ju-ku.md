MySQ连接

```
[root@host]# mysql -u root -p
Enter password:******
```

MySQL创建数据库

```
[root@host]# mysqladmin -u root -p create RUNOOB
Enter password:******
```

MySQL选择数据库

```
[root@host]# mysql -u root -p
Enter password:******
mysql> use RUNOOB;
Database changed
mysql>
```

MySQL删除数据库

```
[root@host]# mysqladmin -u root -p drop RUNOOB
Enter password:******
```




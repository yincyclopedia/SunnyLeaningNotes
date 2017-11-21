## MySQL创建数据表

 创建MySQL数据表需要以下信息：

* 表名
* 表字段名
* 定义每个表字段

通用语法：

```
CREATE TABLE table_name (column_name column_type);
```

实例：

    CREATE TABLE IF NOT EXISTS `runoob_tbl`(
       `runoob_id` INT UNSIGNED AUTO_INCREMENT,
       `runoob_title` VARCHAR(100) NOT NULL,
       `runoob_author` VARCHAR(40) NOT NULL,
       `submission_date` DATE,
       PRIMARY KEY ( `runoob_id` )
    )ENGINE=InnoDB DEFAULT CHARSET=utf8;

实例解析：

* 如果你不想字段为 **NULL**可以设置字段的属性为 **NOT NULL**， 在操作数据库时如果输入该字段的数据为**NULL**，就会报错。
*  AUTO\_INCREMENT定义列为自增的属性，一般用于主键，数值会自动加1。
*  PRIMARY KEY关键字用于定义列为主键。 您可以使用多列来定义主键，列间以逗号分隔。
* ENGINE 设置存储引擎，CHARSET 设置编码。

## 通过命令提示符创建表

通过 mysql&gt; 命令窗口可以很简单的创建MySQL数据表。你可以使用 SQL 语句 **CREATE TABLE** 来创建数据表。

### 实例

以下为创建数据表 runoob\_tbl 实例:

```
root@host# mysql -u root -p
Enter password:*******
mysql> use RUNOOB;
Database changed
mysql> CREATE TABLE runoob_tbl(
   -> runoob_id INT NOT NULL AUTO_INCREMENT,
   -> runoob_title VARCHAR(100) NOT NULL,
   -> runoob_author VARCHAR(40) NOT NULL,
   -> submission_date DATE,
   -> PRIMARY KEY ( runoob_id )
   -> )ENGINE=InnoDB DEFAULT CHARSET=utf8;
Query OK, 0 rows affected (0.16 sec)
mysql>
```

**注意：**

MySQL命令终止符为分号 \(;\) 。

# MySQL 删除数据表

 MySQL中删除数据表是非常容易操作的， 但是你再进行删除表操作时要非常小心，因为执行删除命令后所有数据都会消失。

### 语法

以下为删除MySQL数据表的通用语法：

```
DROP TABLE table_name ;
```

## 在命令提示窗口中删除数据表

 在mysql&gt;命令提示窗口中删除数据表SQL语句为 **DROP TABLE** ：

### 实例

以下实例删除了数据表runoob\_tbl:

```
root@host# mysql -u root -p
Enter password:*******
mysql> use RUNOOB;
Database changed
mysql> DROP TABLE runoob_tbl
Query OK, 0 rows affected (0.8 sec)
mysql>


```




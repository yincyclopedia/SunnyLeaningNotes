# MySQL 插入数据

 MySQL 表中使用 **INSERT INTO** SQL语句来插入数据。

 你可以通过 mysql&gt; 命令提示窗口中向数据表中插入数据，或者通过PHP脚本来插入数据。

### 语法

以下为向MySQL数据表插入数据通用的 **INSERT INTO** SQL语法：

```
INSERT INTO table_name ( field1, field2,...fieldN )
                       VALUES
                       ( value1, value2,...valueN );
```

 如果数据是字符型，必须使用单引号或者双引号，如："value"。

## 通过命令提示窗口插入数据

 以下我们将使用 SQL **INSERT INTO** 语句向 MySQL 数据表 runoob\_tbl 插入数据

### 实例

以下实例中我们将向 runoob\_tbl 表插入三条数据:

```
root@host# mysql -u root -p password;
Enter password:*******
mysql> use RUNOOB;
Database changed
mysql> INSERT INTO runoob_tbl 
    -> (runoob_title, runoob_author, submission_date)
    -> VALUES
    -> ("学习 PHP", "菜鸟教程", NOW());
Query OK, 1 rows affected, 1 warnings (0.01 sec)
mysql> INSERT INTO runoob_tbl
    -> (runoob_title, runoob_author, submission_date)
    -> VALUES
    -> ("学习 MySQL", "菜鸟教程", NOW());
Query OK, 1 rows affected, 1 warnings (0.01 sec)
mysql> INSERT INTO runoob_tbl
    -> (runoob_title, runoob_author, submission_date)
    -> VALUES
    -> ("JAVA 教程", "RUNOOB.COM", '2016-05-06');
Query OK, 1 rows affected (0.00 sec)
mysql>
```

**注意：** 使用箭头标记 -&gt; 不是 SQL 语句的一部分，它仅仅表示一个新行，如果一条SQL语句太长，我们可以通过回车键来创建一个新行来编写 SQL 语句，SQL 语句的命令结束符为分号 ;。

 在以上实例中，我们并没有提供 runoob\_id 的数据，因为该字段我们在创建表的时候已经设置它为 AUTO\_INCREMENT\(自动增加\) 属性。 所以，该字段会自动递增而不需要我们去设置。实例中 NOW\(\) 是一个 MySQL 函数，该函数返回日期和时间。

# MySQL 查询数据

MySQL 数据库使用SQL SELECT语句来查询数据。

 你可以通过 mysql&gt; 命令提示窗口中在数据库中查询数据，或者通过PHP脚本来查询数据。

### 语法

 以下为在MySQL数据库中查询数据通用的 SELECT 语法：

```
SELECT column_name,column_name
FROM table_name
[WHERE Clause]
[OFFSET M ][LIMIT N]
```

* 查询语句中你可以使用一个或者多个表，表之间使用逗号\(,\)分割，并使用WHERE语句来设定查询条件。

* SELECT 命令可以读取一条或者多条记录。
* 你可以使用星号（\*）来代替其他字段，SELECT语句会返回表的所有字段数据
* 你可以使用 WHERE 语句来包含任何条件。
* 你可以通过OFFSET指定SELECT语句开始查询的数据偏移量。默认情况下偏移量为0。
* 你可以使用 LIMIT 属性来设定返回的记录数。






#  MySQL DELETE 语句

 你可以使用 SQL 的 DELETE FROM 命令来删除 MySQL 数据表中的记录。

### 语法

 以下是 SQL DELETE 语句从 MySQL 数据表中删除数据的通用语法：

```
DELETE FROM table_name [WHERE Clause]
```

*  如果没有指定 WHERE 子句，MySQL 表中的所有记录将被删除。

*  你可以在 WHERE 子句中指定任何条件
*  您可以在单个表中一次性删除记录。

## 从命令行中删除数据

这里我们将在 SQL DELETE 命令中使用 WHERE 子句来删除 MySQL 数据表 runoob\_tbl 所选的数据。

### 实例

以下实例将删除 runoob\_tbl 表中 runoob\_id 为3 的记录：

```
mysql> use RUNOOB;
Database changed
mysql> DELETE FROM runoob_tbl WHERE runoob_id=3;
```




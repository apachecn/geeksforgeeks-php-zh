# 在 MySQL

中插入 DATETIME 时的 PHP DATE()格式

> Original: [https://www.geeksforgeeks.org/php-date-format-when-inserting-into-datetime-in-mysql/](https://www.geeksforgeeks.org/php-date-format-when-inserting-into-datetime-in-mysql/)

此问题描述了将日期插入 MySQL 数据库的日期格式。 MySQL 以‘YYYY-MM-DD HH：MM：SS’格式检索和显示日期时间值。 日期只能以此格式存储。 但是，它可以与任何时间格式功能一起使用来更改和显示它。

当使用 PHP 在 MySQL 中编写查询时，将根据 MySQL 本身检查其适用性。 因此，请使用 MySQL 提供的默认日期和时间格式。 ‘YYYY-MM-DD’

**示例：**

```php
DATE: YYYY-MM-DD
Example: 2005-12-26

DATETIME: YYYY-MM-DD HH:MI:SS
Example: 2005-12-26 23:50:30

TIMESTAMP: YYYY-MM-DD HH:MI:SS
Example: 2005-12-26 23:50:30

YEAR: YYYY or YY

```

**创建数据库的 MySQL 查询：**

```php
CREATE DATABASE Date_time_example;

```

**示例 1：**创建数据库和表的 PHP 程序

## PHP

```php
<?php

$servername = "localhost";
$username = "root";
$password = "";
$dbname = "geeks";

// Create connection
$conn = mysqli_connect( $servername, $username, $password, $dbname );

// Check connection
if ( !$conn ) {
    die("Connection failed: " . mysqli_connect_error());
}

// SQL query to create table
$sql = "CREATE TABLE date_test (
    id INT AUTO_INCREMENT PRIMARY KEY,
    created_at DATETIME
)";

if (mysqli_query($conn, $sql)) {
    echo "Table date_test created successfully";
} else {
    echo "Error creating table: " . mysqli_error($conn);
}

// Close connection
mysqli_close($conn);
?>
```
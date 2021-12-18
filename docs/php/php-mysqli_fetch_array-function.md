# PHP|mysqli_fetch_array()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_fetch_array-function/](https://www.geeksforgeeks.org/php-mysqli_fetch_array-function/)

**mysqli_fetch_array()函数**用于从数据库获取行，并将其存储为数组。 该数组可以作为关联数组、数值数组或两者都读取。

关联数组是索引是表的各个列的名称的数组。 另一方面，数字数组是索引为数字的数组，0 表示 n 列表的第一列，n-1 表示最后一列。

**语法：**

```php
mysqli_fetch_array ("database_name", "mode")

```

**参数：**此函数接受上述两个参数，如下所述：

*   **DATABASE_NAME：**它是正在执行操作的数据库。 这是必选参数。
*   **模式：**它可以有三个值-MYSQLI_ASSOC、MYSQLI_NUM 和 MYSQLI_BOTH。 MYSQLI_ASSOC 使函数的行为类似于 mysqli_Fetch_Assoc()函数，读取关联数组；MYSQLI_NUM 使函数的行为类似于 mysqli_Fetch_row()函数，读取数值数组，而 MYSQLI_Both 将读取的数据存储在可以使用列索引和列名访问的数组中。

**程序：**

```php
<?php

$conn = mysqli_connect(
    "localhost", "root", "", "Persons"); 

// Check connection 
if (mysqli_connect_errno()) { 
    echo "Database connection failed."; 
} 

$sql = "SELECT Lastname, Age FROM Persons ORDER BY Lastname";
$result -> $mysqli -> query($sql);

// Numeric array
$row = mysqli_fetch_array($conn, MYSQLI_NUM);
printf ("%s (%s)\n", $row[0], $row[1]);

printf("\n");

// Associative array
$row = mysqli_fetch_array($conn, MYSQLI_ASSOC);
printf ("%s (%s)\n", $row["Firstname"], $row["Lastname"]);

mysqli_close($conn);
?>
```

![](img/254dd351be7273345b5cb73a0f0a8192.png)

对于上表，输出将为：
**输出**：

```php
A    B
C    D
E    F
G    H

A    B
C    D
E    F
G    H

```
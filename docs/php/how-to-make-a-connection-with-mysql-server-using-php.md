# 如何使用 PHP 与 MySQL 服务器建立连接？

> 原文:[https://www . geeksforgeeks . org/如何使用 php 与 mysql 服务器建立连接/](https://www.geeksforgeeks.org/how-to-make-a-connection-with-mysql-server-using-php/)

[MySQL](https://www.geeksforgeeks.org/mysql-common-mysql-queries/) 是一个广泛使用的数据库管理系统，可用于为各种项目提供动力。它的主要销售特点之一是它能够不费力地管理大量数据。有两种方法可以用来连接 MySQL 和 [PHP](https://www.geeksforgeeks.org/php-tutorials/) 代码，下面会提到。

*   [PDO (PHP 数据对象)](https://www.geeksforgeeks.org/php-mysql-database-introduction/)
*   [MySQL 扩展](https://www.geeksforgeeks.org/mysqli-procedural-functions/)

让我们进一步了解这两种选择。

数据库抽象层是 PHP 数据对象(PDO)的扩展。它充当后端与 MySQL 数据库交互的用户界面，并在不改变 PHP 代码的情况下进行更改。它还允许您同时处理多个数据库。使用 PDO 的主要好处是它使你的代码保持简单和可移植。

**MySQL**是一个连接器函数，将 PHP 应用的后端连接到 MySQL 数据库。它的执行方式与上一版本相同，但它更安全、更快，拥有更全面的功能和扩展集合。用 PHP 5.0.0 推出了 MySQLi，驱动安装了 PHP 5.3.0。创建该应用编程接口是为了与 MySQL 版本 4.1.13 和更高版本一起工作。

**连接 MySQL:** 在能够访问 MySQL 数据库中的数据之前，需要能够连接到服务器。使用[**MySQL _ connect()**](https://www.geeksforgeeks.org/php-mysqli_connect-function/)功能根据您的连接方式建立数据库连接。该函数返回一个数据库连接指针，也称为数据库句柄。这个句柄将在后面的代码中使用。获得句柄后，记得添加数据库凭据。

**1。通过 PDO 连接–**在下面的 PDO 示例中也提供了一个数据库(“极客数据库”)。要连接到数据库，PDO 需要一个有效的数据库，否则会引发异常。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$servername = "localhost";
$username = "user";
$password = "123456";
$dbName = "geeksDatabase";

try {

    // Creating the connection
    $conn = new PDO("mysql:host=$servername;dbname=$dbName", 
                    $username, $password);

    // Setting the PDO error mode to exception
    $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    echo "Connection established successfully...";

    // To close the connection
    $conn = null;
} 

// If connection fails 
catch(PDOException $e) {

      // Throws the error message 
    echo "Connection failed: " . $e->getMessage();
}

?>
```

**输出:**

```php
Connection established successfully...
```

**2。通过 MySQLi 连接–**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$servername = "localhost";
$username = "user";
$password = "123456";
$dbName = "geeksDatabase";

// Creating connection
$conn = mysqli_connect($servername, 
         $username, $password, $dbName);

// Checking connection
if (!$conn) {

      // If connecting fails
    die("Connection failed: " . mysqli_connect_error());
}

echo "Connection established successfully...";

// Close the connection  
mysqli_close($conn);

?>
```

**输出:**

```php
Connection established successfully...
```
# 将 PHP 连接到 MySQL

> 原文:[https://www.geeksforgeeks.org/connect-php-to-mysql/](https://www.geeksforgeeks.org/connect-php-to-mysql/)

**我们如何将 PHP 连接到 MySQL？**

PHP 5 及更高版本可以使用以下方式处理 MySQL 数据库:

*   MySQLi 扩展(I 是改良的缩写)
*   PDO

**应该用 MySQLi 还是 PDO？**

MySQLi 和 PDO 都有自己的回报:

*   PDO 将使用 12 种不同的数据库系统，而 MySQL 将只使用 MySQL 数据库。
*   因此，如果你不得不改变你的项目来使用替代数据库，PDO 使这个过程变得容易。您只需要更改连接字符串和一些查询。使用 MySQLi，您将需要重写完整的代码——包括查询。
*   两者都是面向对象的，但是 MySQLi 也提供了一个过程化的 API。

简而言之，如果你想坚持使用 MySQL，你可以选择你想要的，否则你应该选择 PDO。

**使用 MySQL 连接到 MySQL**

这可以通过两种方式实现:

**MySQL 面向对象**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$servername = "localhost";
$username = "username";
$password = "password";

// Connection
$conn = new mysqli($servername,
           $username, $password);

// For checking if connection is
// successful or not
if ($conn->connect_error) {
  die("Connection failed: "
      . $conn->connect_error);
}
echo "Connected successfully";
?>
```

**MySQL 程序化**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$servername = "localhost";
$username = "username";
$password = "password";

// Connection
$conn = mysqli_connect($servername,
               $username, $password);

// Check if connection is
// Successful or not
if (!$conn) {
  die("Connection failed: "
      . mysqli_connect_error());
}
echo "Connected successfully";
?>
```

**使用 PDO** 连接到 MySQL

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$servername = "localhost";
$username = "username";
$password = "password";

try {
      $conn = new PDO(
        "mysql:host=$servername;dbname=myDB",
        $username, $password);

      // Set the PDO error mode
      // to exception
      $conn->setAttribute(PDO::ATTR_ERRMODE,
                  PDO::ERRMODE_EXCEPTION);

      echo "Connected successfully";
} catch(PDOException $e) {
      echo "Connection failed: "
        . $e->getMessage();
}
?>
```
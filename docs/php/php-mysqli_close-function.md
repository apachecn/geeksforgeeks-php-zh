# PHP|mysqli_close()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_close-function/](https://www.geeksforgeeks.org/php-mysqli_close-function/)

**MySQLi 过程过程：**
要关闭 MySQL 数据库中的连接，我们使用 php 函数 mysqli_close()，该函数断开与数据库的连接。 它需要一个参数，该参数是 mysql_connect 函数返回的连接。

**语法：**

```
mysqli_close(conn);
```

如果未在 mysqli_close()函数中指定该参数，则关闭最后打开的数据库。 如果成功关闭连接，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 mysqli_close()函数

```
<?php
$servername = "localhost";
$username = "username";
$password = "password";

// Creating connection
$conn = mysqli_connect($servername, $username, $password);

// Checking connection
if (!$conn) {
    die("Connection failed: " . mysqli_connect_error());
}

// Creating a database named newDB
$sql = "CREATE DATABASE newDB";
if (mysqli_query($conn, $sql)) {
    echo "Database created successfully with the name newDB";
} else {
    echo "Error creating database: " . mysqli_error($conn);
}

// closing connection
mysqli_close($conn);

?>
```

**MySQLi 面向对象过程：：**

要关闭 MySQL 数据库中的连接，我们使用 php 函数 Conn->Close()，该函数断开与数据库的连接。

**语法：**

```
conn->close();
```

**程序：**说明面向对象过程中连接的关闭。

```
<?php
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "newDB";

// checking connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
//Close the connection
$conn->close();
?>
```

**使用 PDO 过程：**
在 PDO 过程中关闭 MySQL 数据库中的连接，我们将连接名称设置为 NULL，这将断开与数据库的连接。

**语法：**

```
conn=null;
```

**程序：**说明 PDO 过程中的连接关闭。

```
<?php
$servername = "localhost";
$username = "username";
$password = "password";

try {
    $conn = new PDO("mysql:host=$servername;dbname=newDB", 
                     $username, $password);

    // setting the PDO error mode to exception
    $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

    $sql = "CREATE DATABASE newDB";

    // using exec() because no results are returned
    $conn->exec($sql);

    echo "Database created successfully with the name newDB";
    }
catch(PDOException $e)
    {
    echo $sql . "
" . $e->getMessage();
    }
$conn = null;
?>
```

**引用：**[http://php.net/manual/en/mysqli.close.php](http://php.net/manual/en/mysqli.close.php)
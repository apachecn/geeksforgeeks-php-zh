# PHP|MySQL 选择查询

> Original: [https://www.geeksforgeeks.org/php-mysql-select-query/](https://www.geeksforgeeks.org/php-mysql-select-query/)

SQL**SELECT**语句用于从数据库表中选择记录。

**语法：**
SELECT 子句的基本语法是-
![](img/7f783e8d113765078f4f8ad66e296122.png)

要选择表中的所有列，请使用![ * ](img/1a2ddf623f239b7e33fcef58fe0db6d8.png "Rendered by QuickLaTeX.com")字符。
![](img/76509d8aaf3f224ada8e5668cfd9b131.png)

**Select 查询的实现：**
让我们考虑下面的表‘data’，它有三列‘FirstName’、‘LastName’和‘Age’。
![](img/929bbf0a6c40b114beaa4a4ff2186050.png)

要选择存储在‘Data’表中的所有数据，我们将使用下面提到的代码。

**使用程序方法选择查询：**

```php
<?php 
$link = mysqli_connect("localhost", "root", "", "Mydb");

if ($link == = false) {
    die("ERROR: Could not connect. "
                .mysqli_connect_error());
}

$sql = "SELECT * FROM Data";
if ($res = mysqli_query($link, $sql)) {
    if (mysqli_num_rows($res) > 0) {
        echo "<table>";
        echo "<tr>";
        echo "<th>Firstname</th>";
        echo "<th>Lastname</th>";
        echo "<th>age</th>";
        echo "</tr>";
        while ($row = mysqli_fetch_array($res)) {
            echo "<tr>";
            echo "<td>".$row['Firstname']."</td>";
            echo "<td>".$row['Lastname']."</td>";
            echo "<td>".$row['Age']."</td>";
            echo "</tr>";
        }
        echo "</table>";
        mysqli_free_res($res);
    }
    else {
        echo "No matching records are found.";
    }
}
else {
    echo "ERROR: Could not able to execute $sql. "
                                .mysqli_error($link);
}
mysqli_close($link);
?>
```

**输出：**
![](img/929bbf0a6c40b114beaa4a4ff2186050.png)

**代码说明：**

1.  “res”变量存储函数*mysql_query()*返回的数据。
2.  每次调用*mysqli_fetch_array()*时，它都会返回*res()*集合中的下一行。
3.  WHILE 循环用于遍历表“DATA”的所有行。

**使用面向对象方法选择查询：**

```php
<?php
$mysqli = new mysqli("localhost", "root", "", "Mydb");

if ($mysqli == = false) {
    die("ERROR: Could not connect. "
                          .$mysqli->connect_error);
}

$sql = "SELECT * FROM Data";
if ($res = $mysqli->query($sql)) {
    if ($res->num_rows > 0) {
        echo "<table>";
        echo "<tr>";
        echo "<th>Firstname</th>";
        echo "<th>Lastname</th>";
        echo "<th>Age</th>";
        echo "</tr>";
        while ($row = $res->fetch_array()) 
        {
            echo "<tr>";
            echo "<td>".$row['Firstname']."</td>";
            echo "<td>".$row['Lastname']."</td>";
            echo "<td>".$row['Age']."</td>";
            echo "</tr>";
        }
        echo "</table>";
        $res->free();
    }
    else {
        echo "No matching records are found.";
    }
}
else {
    echo "ERROR: Could not able to execute $sql. "
                                             .$mysqli->error;
}
$mysqli->close();
?>
```

**输出：**
![](img/929bbf0a6c40b114beaa4a4ff2186050.png)

**使用 PDO 方法选择查询：**

```php
<?php 
try {
    $pdo = new PDO("mysql:host = localhost;
                      dbname=mydb", "root", "");
    $pdo->setAttribute(PDO::ATTR_ERRMODE, 
                        PDO::ERRMODE_EXCEPTION);
}
catch (PDOException $e) {
    die("ERROR: Could not connect. ".$e->getMessage());
}
try {
    $sql = "SELECT * FROM Data";
    $res = $pdo->query($sql);
    if ($res->rowCount() > 0) {
        echo "<table>";
        echo "<tr>";
        echo "<th>Firstname</th>";
        echo "<th>Lastname</th>";
        echo "<th>Age</th>";
        echo "</tr>";
        while ($row = $res->fetch()) {
            echo "<tr>";
            echo "<td>".$row['Firstname']."</td>";
            echo "<td>".$row['Lastname']."</td>";
            echo "<td>".$row['Age']."</td>";
            echo "</tr>";
        }
        echo "</table>";
        unset($res);
    }
    else {
        echo "No matching records are found.";
    }
}
catch (PDOException $e) {
    die("ERROR: Could not able to execute $sql. "
                                .$e->getMessage());
}
unset($pdo);
?>
```

**输出：**
![](img/929bbf0a6c40b114beaa4a4ff2186050.png)
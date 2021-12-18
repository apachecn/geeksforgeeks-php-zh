# PHP|MySQL ORDER BY 子句

> Original: [https://www.geeksforgeeks.org/php-mysql-order-clause/](https://www.geeksforgeeks.org/php-mysql-order-clause/)

**ORDER BY**子句可以与 SELECT 语句一起使用，以按顺序对特定字段的数据进行排序。 它用于按升序或降序对结果集进行排序。

**语法：**
ORDER BY 子句的基本语法是-
![](img/a86232e4a5f19d4bcda75fae029cdc0e.png)

#### 按条款执行订单：

让我们考虑下面的表“Data”，它有三列‘FirstName’、‘LastName’和‘Age’。
![](img/929bbf0a6c40b114beaa4a4ff2186050.png)

要按升序对数据表中的 FirstName 列进行排序，可以使用以下代码。

**使用程序方法的 ORDER BY 子句：**

```php
<?php
$link = mysqli_connect("localhost", "root", "", "Mydb");

if($link === false){
    die("ERROR: Could not connect. " 
                . mysqli_connect_error());
}

$sql = "SELECT * FROM Data ORDER BY Firstname";
if($res = mysqli_query($link, $sql)){
    if(mysqli_num_rows($res) > 0){
        echo "<table>";
            echo "<tr>";
            echo "<th>Firstname</th>";
            echo "<th>Lastname</th>";
            echo "<th>age</th>";
            echo "</tr>";
        while($row = mysqli_fetch_array($res)){
            echo "<tr>";
                echo "<td>" . $row['Firstname'] . "</td>";
                echo "<td>" . $row['Lastname'] . "</td>";
                echo "<td>" . $row['Age'] . "</td>";
            echo "</tr>";
        }
        echo "</table>";
        mysqli_free_result($res);
    } else{
        echo "No matching records are found.";
    }
} else{
    echo "ERROR: Could not able to execute $sql. "
                                . mysqli_error($link);
}
mysqli_close($link);
?>
```

**输出：**
![](img/7a0affe744c53b9c8234a0b405d0ac77.png)

**代码说明：**

1.  “res”变量存储函数*mysql_query()*返回的数据。
2.  每次调用*mysqli_fetch_array()*时，它都会返回*res()*集合中的下一行。
3.  WHILE 循环用于遍历表“DATA”的所有行。

**使用面向对象方法的 ORDER BY 子句：**

```php
<?php
$mysqli = new mysqli("localhost", "root", "", "Mydb");

if($mysqli === false){
    die("ERROR: Could not connect. " 
                . $mysqli->connect_error);
}

$sql = "SELECT * FROM Data ORDER BY Firstname";
if($res = $mysqli->query($sql)){
    if($res->num_rows > 0){
        echo "<table>";
            echo "<tr>";
                echo "<th>Firstname</th>";
                echo "<th>Lastname</th>";
                echo "<th>Age</th>";
            echo "</tr>";
        while($row = $res->fetch_array()){
            echo "<tr>";
                echo "<td>" . $row['Firstname'] . "</td>";
                echo "<td>" . $row['Lastname'] . "</td>";
                echo "<td>" . $row['Age'] . "</td>";
            echo "</tr>";
        }
        echo "</table>";
        $res->free();
    } else{
        echo "No matching records are found.";
    }
} else{
    echo "ERROR: Could not able to execute $sql. " 
                                    . $mysqli->error;
}

$mysqli->close();
?>
```

**输出：**
![](img/7a0affe744c53b9c8234a0b405d0ac77.png)

**使用 PDO 方法的 ORDER BY 子句：**

```php
<?php
try{
    $pdo = new PDO("mysql:host=localhost;
                    dbname=Mydb", "root", "");
    $pdo->setAttribute(PDO::ATTR_ERRMODE, 
                        PDO::ERRMODE_EXCEPTION);
} catch(PDOException $e){
    die("ERROR: Could not connect. " 
                            . $e->getMessage());
}
try{
    $sql = "SELECT * FROM Data ORDER BY Firstname";
    $res = $pdo->query($sql);
    if($res->rowCount() > 0){
        echo "<table>";
            echo "<tr>";
                echo "<th>Firstname</th>";
                echo "<th>Lastname</th>";
                echo "<th>Age</th>";
            echo "</tr>";
        while($row = $res->fetch()){
            echo "<tr>";
                echo "<td>" . $row['Firstname'] . "</td>";
                echo "<td>" . $row['Lastname'] . "</td>";
                echo "<td>" . $row['Age'] . "</td>";
            echo "</tr>";
        }
        echo "</table>";
        unset($res);
    } else{
        echo "No matching records are found.";
    }
} catch(PDOException $e){
    die("ERROR: Could not able to execute $sql. " 
                                    . $e->getMessage());
}

unset($pdo);
?>
```

**输出：**
![](img/7a0affe744c53b9c8234a0b405d0ac77.png)
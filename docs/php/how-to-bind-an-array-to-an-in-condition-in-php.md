# PHP 中如何将数组绑定到 IN()条件？

> 原文:[https://www . geesforgeks . org/如何将数组绑定到 php 中的条件中/](https://www.geeksforgeeks.org/how-to-bind-an-array-to-an-in-condition-in-php/)

给定一个包含一些数据的数据库，任务是使用 MySQL IN()运算符将一个 PHP 数组绑定到它。在这里，我们将看一个程序，它通过在查询中获取一个 PHP 数组并解释它来完成这个任务。

**SQL IN()运算符:**SQL IN()运算符允许在 where 子句中传递多个参数。它经常被用作多个或语句的简写。

**语法:**

```
SELECT <column_name(s)>
FROM <table_name>
WHERE <column_name> IN( value1, value2, ...);
```

**[PHP 内爆()函数](https://www.geeksforgeeks.org/php-implode-function/) :** 我们将使用 PHP 预定义的函数内爆()来处理数组。函数的作用是:用一个字符串连接数组元素。执行相同的操作需要两个参数。首先是用于连接数组元素的字符串，也可以称为粘合字符串。因为它会被用来把元素粘在一起。第二个显然是需要执行操作的数组。

**语法:**

```
*string* implode(separator, array)
```

**数组绑定:**根据我们的需要，我们只需要将 PHP 数组绑定到 in()子句，要获得这个功能，我们首先需要将给定的数组转换成 IN()子句可以接受的形式，这是一个由 PHP 内爆()函数执行的作业。此外，请记住，通过将我们的数组传递给函数，我们只是以 in()可接受的形式转换数组，但它仍然是同一个数组。

以下程序将帮助您更实际、更仔细地理解这个概念:

**Used DataBase:** 这里，我们将使用一个数据库(**数据库名:Geeks** )来绑定一个数组到 PHP 中的 IN()条件。

**表名:GFG** 表名 GFG 包含以下信息。

| 身份证明 | 名字 |
| one | 梅根（人名） |
| Two | 吉娜 |
| three | 达里 |
| four | 初入社交界的 |
| five | 米歇尔 |
| six | 雷切尔 |
| seven | 舱外活动 |
| eight | 地对空导弹 |
| nine | 六便士之硬币 |
| Ten | 定时（timing 的缩写） |

**程序 1:** 下面的代码从 **GFG 表**中获取 PHP 数组的 id，并将其传递给 IN()运算符来检索名称，与给定的 id 相对应。

```
<?php  

// Connecting to the server
$server = 'localhost';
$username = 'root';
$password = '';
$dbname = 'Geeks';

// Declare and initialize an
// array that need to be
// passed to IN() operator
$arr = array(1, 2, 3, 4, 5);

// Joining array elements using
// implode() function
$ids = implode(', ', $arr);

$conn = new mysqli($server, 
    $username, $password, $dbname);

// SQL query to pass the array 
$sql = ('SELECT NAME FROM GFG 
        WHERE ID IN ('.$ids.')' );

$result = $conn->query($sql);

if($result->num_rows > 0) {
    while($row = $result->fetch_assoc()) {
        echo $row['NAME'] . "<br>"; }
}  else {
    echo "0 results";
}

$conn->close();

?>
```

**输出:**

```
MEGAN
GINA
DARVY
DEBBY
MICHEL
```

**程序 2:** 下面的代码使用相同的信息表，但是检索与数组中给出的名称相对应的 ID。

```
<?php

// Connecting to server
$server = 'localhost';
$username = 'root';
$password = '';
$dbname = 'Geeks';

// Declare and initialize an
// array that need to be
// passed to IN() operator
$arr = array("MEGAN", "TIM");

// Joining array elements using
// implode() function
$names = implode('\', \'', $arr);

// Since array elements to be
// searched, here are string
// making it look like a string
// so that sql can easily
// interpret it
$fin = "'" . $names . "'";

$conn = new mysqli($server, 
    $username, $password, $dbname);

// SQL query to pass the array 
$sql=('SELECT ID FROM GFG
        WHERE NAME IN ('.$fin.')' );

$result = $conn->query($sql);

if($result->num_rows > 0)  {
    while($row = $result->fetch_assoc()){
        echo $row['ID'] . "<br>"; 
    }
} else {
    echo "0 results";
}

$conn->close();

?>
```

**输出:**

```
1
10
```
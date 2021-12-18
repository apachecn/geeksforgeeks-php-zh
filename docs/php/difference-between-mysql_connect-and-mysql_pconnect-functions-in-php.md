# PHP 中 mysql_connect()和 mysql_pconnect()函数的区别

> 原文:[https://www . geesforgeks . org/区别-MySQL _ connect-and-MySQL _ pconnect-functions-in-PHP/](https://www.geeksforgeeks.org/difference-between-mysql_connect-and-mysql_pconnect-functions-in-php/)

**mysql_connect()函数:**使用 **mysql_connect()** 函数与数据库建立新的连接。这个连接是在脚本开始执行时建立的。在建立与数据库的连接之后，它将是有效的，或者仅在脚本执行之前才与数据库连接。这意味着一旦脚本停止执行，与数据库的连接也将关闭。 **mysql_close()** 方法用于关闭与数据库的连接。

**示例 1:** 在下面的代码中，如果连接成功，它将显示回声部分，或者如果出现任何错误，它将显示芯片部分。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

mysqli_connect("localhost", "gaurav", "", "GeeksForGeeks");

if(mysqli_connect_error())
    echo "Connection Error.";
else
    echo "Database Connection Established Successfully.";

?>
```

```
Database Connection Established Successfully.
```

**示例 2:** 在下面的代码中，我们正在连接到端口 3307 上的 geeksforgeeks.org 数据库。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// We connect to geeksforgeeks.org and port 3307
$link = mysql_connect(
  'geeksforgeeks.org:3307', 'Gaurav', 'GFG');

if (!$link) {
    die('Could not connect: ' . mysql_error());
}

echo 'Connected successfully to GFG Database';

mysql_close($link);
?>
```

```
Connected successfully to GFG Database
```

**MySQL _ pcconnect()函数:****MySQL _ pcconnect()**是一种与 **mysql_connect()略有不同的函数。**当您使用此功能连接到数据库时，它将使用相同的*用户名*和*密码*搜索是否有任何其他现有的数据库连接，如果此条件显示为*真*，则它返回资源标识。每当调用脚本时，它不会一次又一次地建立连接，并且当脚本停止执行时，它也不会结束连接。这种类型的连接称为持久连接。

**示例 1:** 在下面的代码中，我们正在使用 mysql_pconnect()函数建立持久连接。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$con = mysql_pconnect(
      "localhost", "mysql_user", "mysql_pwd");

if (!$con) {
      die('Could not connect: ' . mysql_error());
}
else {
      echo("Persistent Connection Established");
}
?>
```

```
Persistent Connection Established
```

**示例 2:** 在下面的代码中，我们使用持久连接(mysql_pconnect())连接到端口 3307 上的 geeksforgeeks.org 数据库。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// We connect to geeksforgeeks.org
// and port 3307
$link = mysql_pconnect(
  'geeksforgeeks.org:3307', 'Gaurav', 'GFG');

if (!$link) {
    die('Could not connect: ' . mysql_error());
}

echo 'Connected successfully to GFG '
  . 'Database using Persistent Connection';

mysql_close($link);

?>
```

```
Connected successfully to GFG Database using Persistent Connection
```

**MySQL _ connect()与 mysql_pconnect()函数的区别:**

<figure class="table">

| 

**MySQL _ connect()函数**

 | 

**MySQL _ pconnect()函数**

 |
| --- | --- |
| This function establishes a connection with the database when calling the script. | This function first checks whether a connection with the same *user name* and *password* has been created, and if not, a connection is established. |
| **MySQL _ close ()** method is used to close the connection with the database. | **MySQL _ close ()** Do not close the connection with the database. |
| This is a time-consuming function, because it establishes a connection every time it is called. | This is a time-saving function, because it does not establish a connection every time it is called, but only performs a connection establishment once. |
| Used when establishing a new connection. | Use it when we don't want to disconnect from the database and keep it for future use. |
| It needs more memory, because every time this function is called, a connection is established. | Since the connection is only established once |
| It needs less memory, and is not user-friendly because of its complex use. | Because of its simplicity, it is more user-friendly. |
| Use the **myql _ connect ()** method to open the database every time the page is loaded. | Every time the page is loaded with **MySQL _ pconnect ()** method, the database will not be opened. |

</figure>
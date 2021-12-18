# PHP|mysqli_error()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_error-function/](https://www.geeksforgeeks.org/php-mysqli_error-function/)

函数**mysqli_error()**用于返回最近失败的 MySQL 函数调用中的错误。 如果有多个 MySQL 函数调用，则最后一条语句中的错误是函数指出的错误。

**语法：**

```
mysqli_error("database_name")

```

**参数：**此函数接受上述单个参数，如下所述：

*   **DATABASE_NAME：**它是正在执行操作的数据库。 这是必选参数。

**程序 1：**

```
<?php
$conn = mysqli_connect(
    "localhost", "root", "", "Persons"); 

// Check connection 
if (mysqli_connect_errno()) { 
    echo "Database connection failed."; 
} 

// Check for error in query
if (!mysqli_query($link, "SET Age=1")) {
    printf("Error message: %s\n", mysqli_error($conn));
}    

mysqli_close($conn);
?>
```

假设要在下面给出的表上执行操作：

![](img/254dd351be7273345b5cb73a0f0a8192.png)

**输出将为：**

```
Error message: Unknown system variable 'Age'

```

**程序 2：**

```
<?php
$conn = mysqli_connect(
    "localhost", "root", "", "Persons"); 

// Check connection 
if (mysqli_connect_errno()) { 
    echo "Database connection failed."; 
} 

// Check for error in query
if (!mysqli_query($link, "SET Firstname='Arkadyuti'")) {
    printf("Error message: %s\n", mysqli_error());
}    

mysqli_close($conn);
?>
```

发帖主题：Re：Колибри0.7.0

```
Error message: mysqli_error() expects exactly 1 parameter, 0 given

```

这个示例还演示了 mysqli_error()需要一个数据库作为参数。
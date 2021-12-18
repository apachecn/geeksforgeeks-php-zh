# PHP|mysqli_num_row()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_num_rows-function/](https://www.geeksforgeeks.org/php-mysqli_num_rows-function/)

Mysqli_num_row()函数是 PHP 中的一个内置函数，用于返回结果集中的行数。 它通常用于检查数据库中是否存在数据。 要使用此功能，必须先建立与 MySQL 数据库的连接。

**语法：**

```php
mysqli_num_rows ( $result );

```

**参数：**此函数接受单个参数$result(其中$result 是使用 mysqli_query()设置的 MySQL 查询)。 必选参数，表示 MySQL 中 FETCH 查询返回的结果集。

**返回值：**它返回结果集中的行数。 如果没有与给定条件匹配的行，则返回 False。

假设在名为*Geek*的 MySQL 数据库中有一个名为*Geek*的表。 下面是对桌上极客的描述。

| 用户名 | 密码 / 口令 |
| 极客 1 | 通行证 1 |
| 极客 2。 | 护照 2 |
| 极客 3。 | 护照 3 |
| 极客 4 | 通行证 4 |

下面的程序演示了 PHP 中的 mysqli_num_row()函数。

```php
<?php
    // Setting up connection with database Geeks
    $connection = mysqli_connect("localhost", "root", "", 
                                                 "Geeks");

    // Check connection
    if (mysqli_connect_errno())
    {
        echo "Database connection failed.";
    }

    // query to fetch Username and Password from
    // the table geek
    $query = "SELECT Username, Password FROM geek";

    // Execute the query and store the result set
    $result = mysqli_query($connection, $query);

    if ($result)
    {
        // it return number of rows in the table.
        $row = mysqli_num_rows($result);

           if ($row)
              {
                 printf("Number of row in the table : " . $row);
              }
        // close the result.
        mysqli_free_result($result);
    }

    // Connection close 
    mysqli_close($connection);
?>
```

发帖主题：Re：Колибри0.7.8.0

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
# PHP|ftp_close()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_close-function/](https://www.geeksforgeeks.org/php-ftp_close-function/)

函数的作用是：关闭已经存在的到指定 FTP 服务器或主机的 FTP 连接。

**语法：**

```php
ftp_close( $ftp_connection );
```

**参数：**此函数接受必需的单个参数**$ftp_connection**。 指定关闭 FTP 连接的 FTP 连接。

**返回值：**成功返回 True，失败返回 False。

**注意：**

*   This function applies to PHP 4.0.0 and later.
*   The following example cannot be run on the online IDE. So try running on some PHP managed servers or local hosts with the correct ftp server name.

下面的程序演示了 PHP 中的 ftp_lose()函数：

**示例 1：**

```php
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Establishing ftp connection 
$ftp_connection = ftp_connect($ftp_server) 
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "Successfully connected to the ftp server!";

    // Closing  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**使用端口 21 连接到 ftp 服务器。

```php
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Establishing ftp connection 
$ftp_connection = ftp_connect($ftp_server, 21) 
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "Successfully connected to the ftp server!";

    // Closing  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.ftp-close.php](https://www.php.net/manual/en/function.ftp-close.php)
# PHP|ftp_raw()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_raw-function/](https://www.geeksforgeeks.org/php-ftp_raw-function/)

Ftp_raw()函数是 PHP 中的一个内置函数，用于向远程服务器(即 FTP 服务器)发送原始命令。

**语法：**

```
ftp_raw( $ftp_connection, $command )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定已经存在的 FTP 连接。
*   **$COMMAND：**必选参数。 它指定要在 FTP 服务器上执行的命令。

**返回值：**它以字符串数组的形式返回服务器的响应。 返回原始数据，则不执行解析。 它对确定是否执行命令没有帮助。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

**示例：**

## PHP

```
<?php

// Connect to FTP server

// Use a correct ftp server
$ftp_server = "localhost";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
        or die("Could not connect to $ftp_server");

if($ftp_connection) {

    // Storing response from ftp_raw() in $response
    $response = ftp_raw($ftp_connection, "USER abc");

    // Printing $response with print_r()
    print_r($response);  

    // Closing  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [0] => 331 Password required for abc ) 
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-raw.php](https://www.php.net/manual/en/function.ftp-raw.php)
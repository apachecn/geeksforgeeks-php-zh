# PHP|ftp_get_option()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_get_option-function/](https://www.geeksforgeeks.org/php-ftp_get_option-function/)

函数的作用是：获取现有 FTP 连接的运行时选项。

**语法：**

```
ftp_get_option( $ftp_connection, $option )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定已经存在的 FTP 连接。
*   **$OPTION：**必选参数。 它指定为现有 FTP 连接返回的运行时选项。
    *   FTP_TIMEOUT_SEC：返回网络使用的超时时间。
    *   FTP_AUTOSEEK：如果此选项为 ON，则返回，否则返回 FALSE。

**返回值：**成功时返回选项的值，不支持则返回 False。

**注：**

*   此函数适用于 PHP 4.2.0 及更高版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

**示例：**

## PHP

```
<?php

// Connect to FTP server

// Use a correct ftp server
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username="username";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="password";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
        or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!";

        // Printing timeout for current ftp connection
        echo ftp_get_option($ftp_connection, FTP_TIMEOUT_SEC) . "<br>";

        // Printing whether FTP_AUTOSEEK enabled or not
        echo ftp_get_option($ftp_connection, FTP_AUTOSEEK) . "<br>";

    }
    else {
        echo "<br>login failed!";
    }

    // Closing  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
successfully connected to the ftp server!
logged in successfully!
90
1
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-get-option.php](https://www.php.net/manual/en/function.ftp-get-option.php)
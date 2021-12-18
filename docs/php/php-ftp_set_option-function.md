# PHP|ftp_set_option()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_set_option-function/](https://www.geeksforgeeks.org/php-ftp_set_option-function/)

函数**ftp_set_option()**是 PHP 的内置函数，用于设置现有 FTP 连接的运行时选项。

**语法：**

```php
ftp_set_option( $ftp_connection, $option, $value )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定已经存在的 FTP 连接。
*   **$OPTION：**必选参数。 它指定要为现有 FTP 连接设置的运行时选项。$OPTION 的可能值为：
    *   FTP_TIMEOUT_SEC：返回网络使用的超时时间。
    *   FTP_AUTOSEEK：默认情况下启用。 如果此选项为开，则返回 TRUE，否则返回 FALSE。
    *   FTP_USEPASVADDRESS：当它设置为 FALSE 时，作为对 PASV 命令的响应，PHP 将忽略 FTP 服务器返回的 IP 地址，而使用该 IP 地址作为 ftp_connect()函数的参数。
*   **$value：**必选参数。 它指定上一个参数中的选项的值。

**返回值：**

*   **成功时：**返回 TRUE，即可以设置选项。
*   **失败时：**返回 FALSE。 还会生成一条警告消息。

**注：**

*   此函数适用于 PHP 4.2.0 及更高版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

**示例：**

## PHP

```php
<?php

// Connect to FTP server

// Use a correct ftp server
$ftp_server = "localhost";

//use correct ftp username
$ftp_username="user";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="user";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
        or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection,
                    $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!<br>";

        // Printing is setting option successful
        // for current ftp connection
        echo ftp_set_option($ftp_connection,
                        FTP_TIMEOUT_SEC, 120);       
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

```php
successfully connected to the ftp server!
logged in successfully!
1
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-set-option.php](https://www.php.net/manual/en/function.ftp-set-option.php)
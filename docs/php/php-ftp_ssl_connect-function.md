# PHP|ftp_ssl_connect()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_ssl_connect-function/](https://www.geeksforgeeks.org/php-ftp_ssl_connect-function/)

函数的作用是：**ftp_ssl_connect()函数**是 PHP 中的一个内置函数，它可以打开安全的 SSL-FTP 连接。 当连接打开时，可以针对服务器运行 FTP 功能。 它打开到参数中指定的主机的显式 SSL-FTP 连接。 即使服务器的证书无效或没有为 SSL-FTP 配置，它也会成功。

**语法：**

```
ftp_ssl_connect($host, $port, $timeout);
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$HOST：**必选参数。 它指定 FTP 服务器地址。 它可以是域地址或 IP 地址。 此参数不应以“ftp：//”为前缀，也不应有任何尾随斜杠。
*   **$port：**这是一个可选参数。 它指定要连接的端口。 如果未提供端口，则使用默认端口，即 21。
*   **$timeout：**它也是一个可选参数。 它指定网络操作的超时时间。 如果未提供，则传递默认值，即 90 秒。

**返回值：**成功返回 SSL-FTP 流，失败返回 False。

**注：**

*   此函数在 PHP 4.0.0 和更新版本上可用。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。
*   只有在 PHP 中静态内置 ftp 模块和 OpenSSL 支持时，此函数才可用。

以下程序说明了 PHP 中的 ftp_ssl_connect()函数：

**示例 1：**

## PHP

```
<?php

// Use ftp_ssl_connect() function to
// check Connection
$conn = ftp_ssl_connect("ftp.testftp.com")
    or die("Could not connect");

echo "Connection established successfully";

?>
```

发帖主题：Re：Колибри0.7.0

```
Connection established successfully
```

**示例 2：**此示例使用 ftp_ssl_connect()函数通过 SSL-FTP 连接登录

## PHP

```
<?php

// Setting up basic SSL connection

// User IP address to which you
// want to connect to
$ftp_server = "8.8.8.8";

// Logging in in the established ftp connection.
$ftp_conn = ftp_ssl_connect($ftp_server)
    or die("Could not connect to $ftp_server");

// Use your username
$ftp_username = "your_username";

// Use your password
$ftp_userpass = "your_password";

$login = ftp_login($ftp_conn, $ftp_username, $ftp_userpass);

if( $login ) {
    echo "Successfully logged in with ".$ftp_server;
}
else {
    echo "Log in failed";
}

// Closing SSL connection
ftp_close($ftp_conn);

?>
```

发帖主题：Re：Колибри0.7.0

```
Successfully logged in with 8.8.8.8
```

**引用：**[https://www.php.net/manual/en/function.ftp-ssl-connect.php](https://www.php.net/manual/en/function.ftp-ssl-connect.php)
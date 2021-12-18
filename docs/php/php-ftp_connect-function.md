# PHP|ftp_connect()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_connect-function/](https://www.geeksforgeeks.org/php-ftp_connect-function/)

Ftp_connect()函数是 PHP 中的一个内置函数，用于创建到指定 FTP 服务器或主机的新连接。 连接成功后，只有其他 FTP 功能可以在服务器上运行。

**语法：**

```php
ftp_connect( $ftp_host, $ftp_port, $timeout );
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$ftp_host：**必选参数，用于指定要连接的主机名或 ftp 服务器。 它可以是域名或 IP 地址，且这些地址不能以“ftp：//”为前缀，也不能在 URL 末尾有任何斜杠。
*   **$ftp_port：**可选参数。 它指定要连接的端口号。 如果未提供，则使用 FTP 的默认端口号。 默认 ftp 端口号为 21。
*   **$timeout：**可选参数。 它指定所有后续网络操作的超时时间。 如果未提供此参数，则使用默认参数，即 90 秒。

**注意：可以相应地使用 ftp_get_option()和 ftp_set_option()随时查询或更改**超时。

**返回值：**成功返回 FTP 流，失败返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

以下程序说明了 PHP 中的 ftp_connect()函数：

**示例 1：**

## PHP

```php
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Establish ftp connection
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "Successfully connected to the ftp server!";

    // Closing  connection
    ftp_close($ftp_connection);
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
Successfully connected to the ftp server!
```

**示例 2：**使用端口 21 连接到 ftp 服务器。

## PHP

```php
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Establish ftp connection
$ftp_connection = ftp_connect($ftp_server, 21)
    or die("Could not connect to $ftp_server");

// Port number 21 is used as second parameter
// in the function ftp_connect()
if( $ftp_connection ) {
    echo "Successfully connected to the ftp server!";

    // Closing  connection
    ftp_close( $ftp_connection );
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
Successfully connected to the ftp server!
```

**引用：**[https://www.php.net/manual/en/function.ftp-connect.php](https://www.php.net/manual/en/function.ftp-connect.php)
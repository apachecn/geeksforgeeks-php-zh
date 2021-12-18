# PHP|ftp_login()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_login-function/](https://www.geeksforgeeks.org/php-ftp_login-function/)

Ftp_login()函数是 PHP 中的一个内置函数，用于登录到已建立的 FTP 连接。

**语法：**

```
ftp_login( $ftp_connection, $ftp_username, $ftp_userpass );
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定要登录的 FTP 连接。
*   **$ftp_username：**必选参数。 它指定 FTP 连接的用户名。
*   **$ftp_userpass：**必选参数。 它指定该 FTP 连接的用户的密码。

**返回值：**成功返回 True，失败返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此，请尝试使用正确 ftp 服务器主机名、用户名和密码在某些 PHP 托管服务器或本地主机上运行。

以下程序说明了 PHP 中的 ftp_login()函数：
**示例 1：**

```
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Use FTP username
$ftp_username="user";

// Use FTP password 
$ftp_userpass="user";

// Establish ftp connection 
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "Successfully connected to the ftp server!";

    // logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if($login) {
        echo "<br>Logged in successfully!";
    }
    else {
        echo "<br>Login failed!";
    }

    // Closing the connection
    ftp_close($ftp_connection); 
}

?>
```

发帖主题：Re：Колибри0.7.0

```
Successfully connected to the ftp server!
Logged in successfully!

```

**示例 2：**使用端口 21 连接到 ftp 服务器。

```
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Use FTP username
$ftp_username="user";

// Use FTP password 
$ftp_userpass="user";

// Establish ftp connection 
$ftp_connection = ftp_connect($ftp_server, 21) 
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "Successfully connected to the ftp server!";

    // logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if($login) {
        echo "<br>Logged in successfully!";
    }
    else {
        echo "<br>Login failed!";
    }

    // Closing the connection
    ftp_close($ftp_connection); 
}

?>
```

发帖主题：Re：Колибри0.7.0

```
Successfully connected to the ftp server!
Logged in successfully!

```

**引用：**[https://www.php.net/manual/en/function.ftp-login.php](https://www.php.net/manual/en/function.ftp-login.php)
# PHP|ftp_exec()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_exec-function/](https://www.geeksforgeeks.org/php-ftp_exec-function/)

函数的作用是：**ftp_exec()函数**是 PHP 中的内置函数，用于在 FTP 服务器上执行命令。

**语法：**

```php
ftp_exec( $ftp_connection, $command )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于执行 FTP 命令或功能的现有 FTP 连接。
*   **$COMMAND：**必选参数。 它指定要在已成功建立连接的 FTP 服务器上执行的命令。

**返回值：**成功返回 True，失败返回 False。

**注：**

*   此函数适用于 PHP 4.0.3 及更高版本。
*   以下示例不能在联机 IDE 上运行。 因此，请尝试使用正确 ftp 服务器名称、用户名和密码在某些 PHP 托管服务器或本地主机上运行。

**示例：**

## PHP

```php
<?php

// Connect to FTP server
// Use a correct ftp server
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username="username";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="password";

// Command to be executed on FTP server
$command="ls-al > test.txt";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
        or die("Could not connect to $ftp_server");

if( $ftp_connection ) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if( $login ) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!";

        // ftp_exec() executes the command
        if (ftp_exec($ftp_connection, $command)) {
            echo "<br>".$command." has been successfully executed.";
        }
        else {
            echo "<br>Error while executing the command .";
        }
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
ls-al > test.txt has been successfully executed.
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-exec.php](https://www.php.net/manual/en/function.ftp-exec.php)
# PHP|ftp_chdir()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_chdir-function/](https://www.geeksforgeeks.org/php-ftp_chdir-function/)

函数**ftp_chdir()**是 PHP 的内置函数，用于更改 FTP 服务器上的当前目录。

**语法：**

```php
ftp_chdir( $ftp_connection, $directory )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于执行 FTP 命令或功能的现有 FTP 连接。
*   **$directory**：必选参数。 它指定远程服务器中当前目录要更改到的路径。

**返回值：**成功返回 True，失败返回 False。
**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此，请尝试使用正确 ftp 服务器名称、用户名和密码在某些 PHP 托管服务器或本地主机上运行。
*   请确保您有更改目录的权限以及对该目录的访问权限。

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

        // ftp_chdir() changing current directory to "htdocs"
        // remember, you must have folder that will use inside
        // current directory of ftp server.
        // Here htdocs folder exists in ftp server inside
        // base or root directory
        if (ftp_chdir($ftp_connection, "htdocs")) {
            echo "<br>Current directory successfully changed to htdocs.";
        }
        else {
            echo "<br>Error while changing current directory.";
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
Current directory successfully changed to htdocs.
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-chdir.php](https://www.php.net/manual/en/function.ftp-chdir.php)
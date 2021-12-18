# PHP|ftp_delete()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_delete-function/](https://www.geeksforgeeks.org/php-ftp_delete-function/)

函数的作用是：**ftp_delete()函数**是 PHP 的内置函数，用于删除 FTP 服务器上的文件。

**语法：**

```
ftp_delete( $ftp_connection, $file )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于执行 FTP 命令或功能的现有 FTP 连接。
*   **$file：**必选参数。 它指定要删除的服务器的文件路径。

**返回值：**成功返回 TRUE，失败返回 FALSE。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此，请尝试使用正确 ftp 服务器名称、用户名和密码在某些 PHP 托管服务器或本地主机上运行。
*   ★★★确保作为删除参数提供的文件存在，并且登录 ftp 连接的 ftp 用户有权删除，否则会产生错误。

**示例：**

## PHP

```
<?php

// Connect to FTP server

// Assign ftp server to the variable
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username="user";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="user";

// Filename or filename with path to specify
// the file on server to be deleted
$file = "test.txt";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
        or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username and password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!";

        // ftp_delete() function to delete file from FTP server
        if (ftp_delete($ftp_connection, $file)) {
            echo "<br>deletion of " . $file . " is successful.";
        }
        else {
            echo "<br>Error while deleting the file " . $file;
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

```
successfully connected to the ftp server!
logged in successfully!
deletion of ./htdocs/test.txt is successful.
Connection closed Successfully!
```

如果该文件被删除并再次运行相同的程序，只要该文件不存在，因为该文件已经被删除，那么就会出现错误。 输出将如下所示

```
successfully connected to the ftp server!
logged in successfully!
Error while deleting the file ./htdocs/test.txt
Connection closed Successfully!
```

**引用：**[https://www.php.net/manual/en/function.ftp-delete.php](https://www.php.net/manual/en/function.ftp-delete.php)
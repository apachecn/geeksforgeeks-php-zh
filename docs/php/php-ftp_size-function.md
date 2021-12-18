# PHP|ftp_size()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_size-function/](https://www.geeksforgeeks.org/php-ftp_size-function/)

Ftp_size()函数是 PHP 中的一个内置函数，用于获取 FTP 服务器上给定文件的大小。
**语法：**

```php
ftp_size( $ftp_connection, $file_name );
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定文件所在位置要使用的现有 FTP 连接。
*   **$FILE_NAME：**必选参数。 它指定远程服务器(即 FTP 服务器)上的文件或文件路径。

**返回值：**成功返回文件大小，错误返回-1。
**注：**和

*   所有 ftp 服务器都不支持此功能。
*   此函数在 PHP 4.0.0 和更新版本上可用。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

以下示例说明 PHP 中的 ftp_size()函数：
**示例 1：**和

## PHP

```php
<?php

// Connect to FTP server

// Use a correct ftp server
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username="user";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="user";

// File name or path to upload to ftp server
$file = "shiva.jpg";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if( $ftp_connection ) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!";

        // Size of the file using ftp_size() function.
        $file_size = ftp_size($ftp_connection, $file);

        if ($file_size != -1) {
            echo "<br>$file is $file_size bytes.";
        }
        else {
            echo "<br>Error getting file size.";
        }
    }
    else {
        echo "<br>login failed!";
    }

    // echo ftp_get_option($ftp_connection, 1);
    // Closing  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}

?>
```
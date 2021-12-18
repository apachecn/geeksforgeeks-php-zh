# PHP|ftp_alloc()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_alloc-function/](https://www.geeksforgeeks.org/php-ftp_alloc-function/)

函数**ftp_alloc()**是 PHP 的内置函数，用于为 FTP 服务器上传的文件分配空间。
**语法：**和

```php
ftp_alloc( $ftp_connection, $filesize, $result );
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于分配空间和上载文件的现有 FTP 连接。
*   **$filesize：**必选参数。 它以字节为单位指定文件的大小，即要分配的字节数。
*   **$result：**此参数是可选的。 它指定一个变量来在其中存储响应。

**返回值：**成功返回 True，失败返回 False。
**注：**和

*   此函数适用于 PHP 5.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

以下示例说明 PHP 中的 ftp_alloc()函数：
**示例 1：**和

## PHP

```php
<?php

// Connect to FTP server

// Use a correct ftp server
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username = "user";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass = "user";

// File name or path to upload to ftp server
$file = "filetoupload.txt";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if($ftp_connection) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection
    // with ftp username password
    $login = ftp_login($ftp_connection,
            $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully or not
        echo "<br>logged in successfully!";

        // Allocating space for the file as specified
        // i.e. in $file
        if(ftp_alloc($ftp_connection, filesize($file), $result)) {
            echo "<br>space successfully allocated on the FTP server";

            if(ftp_put($ftp_connection,
                "uploadedfile_name_in_server.txt", $file, FTP_ASCII)) {
                echo "<br>Uploaded successful $file.";
            }
            else {
                 echo "<br>Error while uploading $file.";
            }
        }
        else {
            echo "<br>space allocation failed!";  
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
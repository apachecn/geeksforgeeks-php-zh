# PHP|ftp_put()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_put-function/](https://www.geeksforgeeks.org/php-ftp_put-function/)

Ftp_put()函数是 PHP 中的内置函数，用于将文件上传到 FTP 服务器。
**语法：**和

```
ftp_put( $ftp_connection, $remote_file_path, $local_file_path, $mode, $start_position );
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于上载文件的现有 FTP 连接。
*   **$REMOTE_FILE_PATH：**必选参数。 它指定要上传文件的远程服务器(即 FTP 服务器)中的路径。
*   **$LOCAL_FILE_PATH：**必选参数。 它指定要在 FTP 服务器中上载的文件的路径。
*   **$mode：**必选参数。 它指定传输模式。 该参数的值为 FTP_ASCII 或 FTP_BINARY。
*   **$start_position：**可选参数。 它指定远程文件中开始上传的位置。

**返回值：**成功返回 True，失败返回 False。
**注：**和

*   此函数在 PHP 4.0.0 和更新版本上可用。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。

下面的示例说明了如何在 PHP 中使用 ftp_put()函数：
**示例 1：**和

## PHP

```
<?php

// Connect to FTP server
$ftp_server = "localhost";

// Use correct ftp username
$ftp_username="user";

// Use correct ftp password corresponding
// to the ftp username
$ftp_userpass="user";

// File name or path to upload to ftp server
$file = "filetoupload.txt";

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if( $ftp_connection ) {
    echo "Successfully connected to the ftp server!";

    // Logging in to established connection with
    // ftp username password
    $login = ftp_login($ftp_connection, $ftp_username, $ftp_userpass);

    // Checking whether logged in successfully or not
    if($login) {
        echo "<br>logged in successfully!";

        if (ftp_put($ftp_connection,
                "uploadedfile_name_in_server.txt", $file, FTP_ASCII))
        {
          echo "<br>Uploaded successful $file.";
        }
        else {
          echo "<br>Error while uploading $file.";
        }

    }
    else {
        echo "<br>login failed!";
    }

    // Closing the  connection
    if(ftp_close($ftp_connection)) {
        echo "<br>Connection closed Successfully!";
    }
}
?>
```
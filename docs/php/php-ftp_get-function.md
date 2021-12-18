# PHP|ftp_get()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_get-function/](https://www.geeksforgeeks.org/php-ftp_get-function/)

函数**ftp_get()**是 PHP 的内置函数，用于从 FTP 服务器获取或下载文件到本地服务器或机器。

**语法：**

```php
ftp_get( $ftp_connection, $local_file_path, $server_file_path,
                             $mode_of_file_transfer, $starting_position );
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$ftp_connection：**必选参数。 它指定用于从 FTP 服务器下载文件的现有 FTP 连接。
*   **$LOCAL_FILE_PATH：**必选参数。 它指定要将文件下载到的本地服务器或计算机的路径。
*   **$SERVER_FILE_PATH：**它是必需的参数。 它指定要从 FTP 服务器下载的文件的路径。
*   **$mode_of_file_transfer：**必填参数。 它指定传输模式。 该参数的值为 FTP_ASCII 或 FTP_BINARY。
*   **$STARTING_POSITION：**可选参数。 它指定远程文件中开始下载的位置。

**返回值：**成功返回 True，失败返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此请尝试使用正确 ftp 服务器名称在某些 PHP 托管服务器或本地主机上运行。
*   应正确选择模式，即 FTP_ASCII 或 FTP_BINARY

**运行以下代码所需的重要信息：**以下代码不能在联机 IDE 中运行，因为它们不允许与文件交互。 因此，请尝试在 PHP 托管服务器上运行。 确保提供正确的 FTP 服务器、用户名、密码、服务器文件路径和本地文件路径。 如果指定为服务器文件的文件不存在，则会出现错误，因此请确保服务器文件存在。 在这些示例中，名为$SERVER_FILE 的文件将作为本地文件下载到$LOCAL_FILE 中提供的相对路径。

下面的示例说明了 PHP 中的 ftp_get()函数：

**示例 1：**

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

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server)
    or die("Could not connect to $ftp_server");

if( $ftp_connection ) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection
    // with ftp username password
    $login = ftp_login($ftp_connection,
            $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully
        // or not
        echo "<br>logged in successfully!";

        // Name or path of the localfile to
        // where the file to be downloaded
        $local_file = "local_file.txt";

        // Name or path of the server file to
        // be downoaded
        $server_file = "server_file.txt";

        // Downloading the specified server file
        if (ftp_get($ftp_connection, $local_file,
                $server_file, FTP_BINARY)) {
            echo "<br>Successfully downloaded "
               . "from $server_file to $local_file.";
          }
          else {
            echo "<br>Error while downloading from "
                  . "$server_file to $local_file.";
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

发帖主题：Re：Колибри0.7.0

![](img/7340d14197cb0d66b2a21770417c26fb.png)![](img/e747e62ff01145a2c94b03dff4d70554.png)

**示例 2：**从 FTP 服务器下载二进制文件。

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

// Establishing ftp connection
$ftp_connection = ftp_connect($ftp_server, 21)
    or die("Could not connect to $ftp_server");

if( $ftp_connection ) {
    echo "successfully connected to the ftp server!";

    // Logging in to established connection
    // with ftp username password
    $login = ftp_login($ftp_connection,
            $ftp_username, $ftp_userpass);

    if($login) {

        // Checking whether logged in successfully
        // or not
        echo "<br>logged in successfully!";

        // Name or path of the localfile to
        // where the file to be downloaded
        $local_file = "local_file_shiva.jpg";

        // Name or path of the server file to
        // be downoaded
        $server_file = "shiva.jpg";

        // Downloading the specified server file
        if (ftp_get($ftp_connection, $local_file,
                $server_file, FTP_BINARY)) {
            echo "<br>Successfully downloaded from"
                . " $server_file to $local_file.";
          }
          else {
            echo "<br>Error while downloading from"
                . " $server_file to $local_file.";
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

发帖主题：Re：Колибри0.7.0

![](img/704afff8759f2b6e5c10bbdb520820f8.png)![](img/6626c8d8228c1d468ab5a076396c1714.png)

**引用：**[https://www.php.net/manual/en/function.ftp-get.php](https://www.php.net/manual/en/function.ftp-get.php)
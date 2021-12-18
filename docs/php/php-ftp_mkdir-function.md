# PHP|ftp_mkdir()函数

> Original: [https://www.geeksforgeeks.org/php-ftp_mkdir-function/](https://www.geeksforgeeks.org/php-ftp_mkdir-function/)

Ftp_mkdir()函数是 PHP 中的内置函数，用于在 ftp 服务器上创建新目录。 目录一旦创建，就不能再创建。 创建已存在的目录将产生错误。
**语法：**

```php
*string* ftp_mkdir( $ftp_connection, $directory_name )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ftp_connection：**这是必选参数，用于指定要在其上创建目录的 ftp 连接。
*   **$DIRECTORY_NAME：**必选参数，用于指定要创建的目录的名称。

如果要在现有或不存在的目录中创建子目录，则$DIRECTORY_NAME 参数的设置格式为“(父目录名)/(子目录名)/(子目录名的子目录名)/…” 就这样吧。 例如，在 testdirectory 内创建一个名为子目录的目录，则$directory_name=“testdirectory/Child directory”；
**返回值：**它返回成功时创建的目录的名称，失败时返回 False。例如
**注意：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   以下示例不能在联机 IDE 上运行。 因此，请尝试使用正确 ftp 服务器名称以及正确的用户名和密码在某些 PHP 托管服务器或本地主机上运行。

**示例 1：**

## PHP

```php
<?php
// Connecting to ftp server

// Use ftp server address
$fserver = "ftp.gfg.org";

// Use ftp username
$fuser="username";

// Use ftp password
$fpass="password";

// Connect to the ftp server
$f_conn = ftp_connect($fserver) or
    die("Could not connect to $fserver");

// Authenticating to ftp server    
$login = ftp_login($f_conn, $fuser, $fpass);

// Directory name which is to be created
$dir = "testdirectory";

// Creating directory
if (ftp_mkdir($f_conn, $dir)) {

    // Execute if directory created successfully
    echo " $dir Successfully created";
}
else {

    // Execute if fails to create directory
    echo "Error while creating $dir";
}

// Closing ftp connection
ftp_close($f_conn);

?>
```
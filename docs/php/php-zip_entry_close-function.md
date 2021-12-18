# PHP|zip_entry_close()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_close-function/](https://www.geeksforgeeks.org/php-zip_entry_close-function/)

函数的作用是：关闭由 zip_entry_open()函数打开的 zip 存档。 ZIP_ENTRY_CLOSE()会导致流关闭，并且与相应 Zip Archive 条目(可能是 Zip Archive 中的文件或目录)的连接中断。 必须关闭的 zip 条目资源作为参数发送给 zip_entry_lose()函数。

**语法：**

```php
 bool zip_entry_close ( $zip_entry )
```

**参数：**函数的作用是：接受单个参数*$zip_entry*。 它是一个必选参数，用于指定 zip 条目资源。

**返回值：**成功返回 TRUE，失败返回 FALSE。

**错误和异常：**

*   必须首先使用 PHP zip_entry_open()函数打开要关闭的 zip 条目存档，否则 PHP zip_entry_lose()函数会生成 PHP 警告。
*   函数的作用是：如果 zip 存档无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx**

下面的程序演示了 PHP 中的 zip_entry_close()函数：

**程序 1：**

```php
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");
$zip_entry = zip_read($zip_handle);

// Opening a zip entry archive 
zip_entry_open($zip_handle, $zip_entry, "rb");
$file = zip_entry_name($zip_entry);

// Closing a zip entry archive 
$flag = zip_entry_close($zip_entry);

if ($flag == true) 
    echo("Zip Entry Archive: " . $file . " has been closed successfully. ");
else
    echo("Zip Entry Archive: " . $file . " cannot be closed.");

zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Zip Entry Archive: article/content.xlsx has been closed successfully.

```

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx
> gfg.pdf
> image.jpeg**

**程序 2：**

```php
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

if(is_resource($zip_handle)) 
{ 
    while($zip_entry = zip_read($zip_handle)) 
    { 

        // Opening a zip archive entry
        $file = zip_entry_open($zip_handle, $zip_entry, "rb");
        $file_name = zip_entry_name($zip_entry);

        if ($file == true) 
        { 
            echo("Zip Entry Archive: " . $file_name . 
                  " has been opened successfully." . "<br>");

            // Closing a zip archive entry
            $flag = zip_entry_close($zip_entry);

            if ($flag == true) 
                echo("Zip Entry Archive: " . $file_name .
                  " has been closed successfully." . "<br>");
            else
                echo("Zip Entry Archive: " . $file_name .
                              " cannot be closed." . "<br>");
        } 
        else
            echo("Zip Entry Cannot be opened."); 
    } 

    // Closing a zip archive
    zip_close($zip_handle);
}
else
    echo("Failed to Open" . $zip_handle );
?>
```

发帖主题：Re：Колибри0.7.0

```php
Zip Entry Archive: article/content.xlsx has been opened successfully.
Zip Entry Archive: article/content.xlsx has been closed successfully.
Zip Entry Archive: article/gfg.pdf has been opened successfully.
Zip Entry Archive: article/gfg.pdf has been closed successfully.
Zip Entry Archive: article/image.jpeg has been opened successfully.
Zip Entry Archive: article/image.jpeg has been closed successfully.

```

**引用：**[http://php.net/manual/en/function.zip-entry-close.php](http://php.net/manual/en/function.zip-entry-close.php)
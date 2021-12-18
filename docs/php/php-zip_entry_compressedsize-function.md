# PHP|ZIP_ENTRY_COMPRESEDSIZE()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_compressedsize-function/](https://www.geeksforgeeks.org/php-zip_entry_compressedsize-function/)

函数的作用是：在 PHP 中内置函数，用于返回 zip 存档条目中压缩文件的大小。 它可用于检索目录条目的压缩大小。 必须读取的 zip 条目资源作为参数发送给 zip_entry_compressedsize()函数，如果成功，它将返回压缩大小。

**语法：**

```php
int zip_entry_compressedsize ( $zip_entry )
```

**参数：**函数的作用是：接受单个参数*$zip_entry*。 它是一个必选参数，用于指定 zip 条目资源。

**返回值：**成功时返回压缩大小。

**错误和异常**：

*   只在成功时才返回文件或目录的压缩大小，否则返回 PHP 警告。
*   函数的作用是：如果 zip 存档无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩档案为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_entry_compressedsize()函数：

**程序 1：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx**

```php
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

$zip_entry = zip_read($zip_handle);

// Reading a zip entry archive 
$file = zip_entry_name($zip_entry);

// Chceking the compressed file size
// of a zip archive entry 
$file_size = zip_entry_compressedsize($zip_entry);

echo("File Name: " . $file . " (" . $file_size . " Bytes) ");

zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx (6341 Bytes)

```

**程序 2：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
>  **content.xlsx
> gfg.pdf
> image.jpeg**

```php
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

if(is_resource($zip_handle)) 
{ 
    while($zip_entry = zip_read($zip_handle)) 
    { 
        $file = zip_entry_name($zip_entry);

        // Checking the compressed file size of
        // a zip archive entry 
        $file_size = zip_entry_compressedsize($zip_entry);

        echo "File Name: " . $file . " (" . $file_size 
              . " Bytes) " . "<br>";
     } 

   zip_close($zip_handle);
} 
else
   echo("Zip archive cannot be opened.");
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx (6341 Bytes) 
File Name: article/gfg.pdf (603195 Bytes) 
File Name: article/image.jpeg (155736 Bytes) 

```

**相关文章：**

*   [PHP|zip_entry_close()函数](https://www.geeksforgeeks.org/php-zip_entry_close-function/)
*   [PHP|zip_close()函数](https://www.geeksforgeeks.org/php-zip_close-function/)

**引用：**[http://php.net/manual/en/function.zip-entry-compressedsize.php](http://php.net/manual/en/function.zip-entry-compressedsize.php)
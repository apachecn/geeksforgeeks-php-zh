# PHP|zip_entry_name()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_name-function/](https://www.geeksforgeeks.org/php-zip_entry_name-function/)

函数的作用是：在 PHP 中内置函数，用于返回 zip 存档条目的名称。 Zip 条目资源将被读取并作为参数发送给 zip_entry_name()函数，如果成功，它将返回 zip 条目存档的名称。

**语法：**

```php
*string* zip_entry_name( $zip_entry )
```

**参数：**此函数接受单个参数*$zip_entry*，这是必需的。 用于指定 zip 条目资源。

**返回值：**成功时返回 zip 存档条目的名称。

**错误和异常：**

*   Zip_entry_name()仅在成功时返回 zip 条目存档的名称，否则将返回 PHP 警告。
*   函数的作用是：如果 zip 存档无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_entry_name()函数：

**程序 1：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx**

```php
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

// Reading a zip entry archive 
$zip_entry = zip_read($zip_handle); 

// Reading the name of a zip entry archive
$file = zip_entry_name($zip_entry);
echo("File Name: " . $file);

// Closing the zip archive
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx

```

**程序 2：**

> 假设一个压缩文件 Itle.zip 包含以下文件和目录：
>  **目录：img**
> 
> *   **Geeksforgeeks.png**
> *   **Geeksforgeeks1.png**
> 
> **content.xlsx
> gfg.pdf
> image.jpeg**

```php
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

if(is_resource($zip_handle)) 
{ 
    while($zip_entry = zip_read($zip_handle)) 
    { 
        $file = zip_entry_name($zip_entry);

        // Checking the file name of a zip archive entry 
        $file_name = zip_entry_name($zip_entry);
        echo("File Name: " . $file_name . "<br>");
    }

    // closing the zip archive
   zip_close($zip_handle);
} 
else
    echo("Zip archive cannot be read.");
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx
File Name: article/gfg.pdf
File Name: article/image.jpeg
File Name: article/img/
File Name: article/img/geeksforgeeks.png
File Name: article/img/geeksforgeeks1.png

```

**相关文章：**

*   [PHP|zip_read()函数](https://www.geeksforgeeks.org/php-zip_read-function/)
*   [PHP|zip_close()函数](https://www.geeksforgeeks.org/php-zip_close-function/)
*   [PHP|zip_entry_close()函数](https://www.geeksforgeeks.org/php-zip_entry_close-function/)
*   [PHP|ZIP_ENTRY_COMPRESEDSIZE()函数](https://www.geeksforgeeks.org/php-zip_entry_compressedsize-function/)

**引用：**[http://php.net/manual/en/function.zip-entry-name.php](http://php.net/manual/en/function.zip-entry-name.php)
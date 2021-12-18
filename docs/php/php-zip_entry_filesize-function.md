# PHP|zip_entry_filesize()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_filesize-function/](https://www.geeksforgeeks.org/php-zip_entry_filesize-function/)

函数的作用是：在 PHP 中内置函数，用于在压缩前返回 zip 存档条目的原始文件大小。 将读取 zip 条目资源并将其作为参数发送给 zip_entry_filesize()函数，如果成功，它将以字节为单位返回值。

**语法：**

```php
int zip_entry_filesize( $zip_entry )
```

**参数：**此函数接受单个参数*$zip_entry*，这是必需的。 它是一个指定 Zip 条目资源的参数。

**返回值：**成功时以字节为单位返回值。

**错误和异常：**

*   只有在压缩成功时，zip_entry_filesize()才会返回压缩前文件的大小(以字节为单位)，否则它会返回 PHP 警告。
*   函数的作用是：如果 zip 存档无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

以下程序说明 PHP：
**程序 1：**中的 zip_entry_filesize()函数

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx**

```php
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

// Reading a zip entry archive 
$zip_entry = zip_read($zip_handle); 
$file = zip_entry_name($zip_entry);

// Reading file size before compression
$size = zip_entry_filesize($zip_entry);

// Displaying the file ans its size
echo("File Name: " . $file . "<br>Size:" . $size . " Bytes");
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx
Size: 9420 Bytes

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

        // Checking the file size of a zip 
        // archive entry before compression  
        $size = zip_entry_filesize($zip_entry);
        echo("File Name: " . $file . "<br>Size: " . $size . " Bytes<br>");
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
Size: 9420 Bytes
File Name: article/gfg.pdf
Size: 621936 Bytes
File Name: article/image.jpeg
Size: 159263 Bytes
File Name: article/img/
Size: 0 Bytes
File Name: article/img/geeksforgeeks.png
Size: 751 Bytes
File Name: article/img/geeksforgeeks1.png
Size: 337 Bytes

```

**引用：**[http://php.net/manual/en/function.zip-entry-filesize.php](http://php.net/manual/en/function.zip-entry-filesize.php)
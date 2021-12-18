# PHP|ZIP_ENTRY_COMPRESSION METHOD()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_compressionmethod-function/](https://www.geeksforgeeks.org/php-zip_entry_compressionmethod-function/)

函数的作用是：在 PHP 中内置函数，用于从 zip 存档条目返回文件或目录的压缩方法。 必须读取的 zip 条目资源作为参数发送给 zip_entry_compressionmethod()函数，如果成功，它将返回压缩方法。

压缩方法有七种，如下所示：

*   未压缩
*   收缩（shrink 的过去分词） / shrink 的过去式分词
*   显示
*   减少(1 至 4 个)
*   标记化
*   内爆
*   BZIP2 BZIP2

Zip 存档文件的默认压缩方法是放气。

**语法：**

```
string zip_entry_compressionmethod( $zip_entry )
```

**参数：**此函数接受单个参数*$zip_entry*。 它是一个必选参数，用于指定 zip 条目资源。

**返回值：**如果成功，则返回指定 zip 存档条目的文件或目录的压缩方法，否则返回 PHP 警告。

**错误和异常**

*   只在成功时才返回文件或目录的压缩方法，否则返回 PHP 警告。
*   函数的作用是：如果压缩文件无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩文件为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_entry_compressionmethod()函数：

**程序 1：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **content.xlsx**

```
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

// Reading a zip archive
$zip_entry = zip_read($zip_handle); 
$file = zip_entry_name($zip_entry);

// Checking the  compression method
$comp_type = zip_entry_compressionmethod($zip_entry);
echo("File Name: " . $file . "=>" . $comp_type);

// Closing the zip archive
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```
File Name: article/content.xlsx => deflated

```

**程序 2：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **art.zip
> content.xlsx
> gfg.pdf
> image.jpeg**

```
<?php

// Opening a zip archive
$zip_handle = zip_open("C:/xampp/htdocs/article.zip");

if(is_resource($zip_handle))
{ 
    // Reading a zip archive
    while($zip_entry = zip_read($zip_handle)) 
    { 
        $file = zip_entry_name($zip_entry);

        // Checking the compression method
        $comp_type = zip_entry_compressionmethod($zip_entry);

        echo("File Name: " . $file . "  =>  " . $comp_type . "<br>");
   } 

    // Closing the zip archive
    zip_close($zip_handle);
} 
else
    echo("Zip archive cannot be opened.");

?>
```

发帖主题：Re：Колибри0.7.0

```
File Name: article/art.zip => stored
File Name: article/content.xlsx => deflated
File Name: article/gfg.pdf => deflated
File Name: article/image.jpeg => deflated

```

**相关文章：**

*   [PHP|ZIP_ENTRY_COMPRESEDSIZE()函数](https://www.geeksforgeeks.org/php-zip_entry_compressedsize-function/)
*   [PHP|zip_entry_close()函数](https://www.geeksforgeeks.org/php-zip_entry_close-function/)
*   [PHP|zip_close()函数](https://www.geeksforgeeks.org/php-zip_close-function/)

**引用：**[http://php.net/manual/en/function.zip-entry-compressionmethod.php](http://php.net/manual/en/function.zip-entry-compressionmethod.php)
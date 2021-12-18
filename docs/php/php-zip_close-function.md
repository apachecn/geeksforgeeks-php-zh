# PHP|zip_close()函数

> Original: [https://www.geeksforgeeks.org/php-zip_close-function/](https://www.geeksforgeeks.org/php-zip_close-function/)

函数的作用是：关闭由 zip_open()函数打开的 zip 存档文件。 Zip_lose()会导致流关闭，并断开与相应 Zip 存档的连接。 由 zip_open()函数打开的 zip 资源作为参数发送给 zip_lose()函数，并且不返回值。

**语法：**

```php
void zip_close ( $zip_file )
```

**参数：**zip_lose()函数接受单个参数$zip_file。 这是一个必选参数，指定要关闭的 zip 文件资源。

**返回值：**不返回任何值。

**错误和异常：**

*   必须首先使用 PHP zip_open()函数打开要关闭的 zip 归档文件，否则 PHP zip_lose()函数会生成 PHP 警告。
*   函数的作用是：如果压缩档案无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_lose()函数：

**程序 1：**

```php
<?php

// Opening zip archive's file
$zip_file = zip_open("article.zip");

if(is_resource($zip_file))
{ 
    echo("Zip Archive File is Successfully Opened.");

    // Closing zip archive's handle
    zip_close($zip_file);
} 
else
{
    echo($zip_file . " Archive File Cannot Be Opened");
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
Zip Archive File is Successfully Opened.

```

**程序 2：**

```php
<?php

// Opening zip archive's file
$zip_file = zip_open("article.zip");

if(is_resource($zip_file)) 
{ 
    while($zipfiles = zip_read($zip_file)) 
    { 
        $file_name = zip_entry_name($zipfiles);
        echo("File Name: " . $file_name . "<br>");
    } 

    // Closing zip archive's
    zip_close($zip_file);
} 
else
{
    echo($zip_file . " Archive File Cannot Be Opened");
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: article/content.xlsx
File Name: article/gfg.pdf
File Name: article/image.jpeg

```

**引用：**
[http://php.net/manual/en/function.zip-close.php](http://php.net/manual/en/function.zip-close.php)
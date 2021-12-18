# PHP|MIME_CONTENT_TYPE()函数

> Original: [https://www.geeksforgeeks.org/php-mime_content_type-function/](https://www.geeksforgeeks.org/php-mime_content_type-function/)

MIME_CONTENT_TYPE()函数是 PHP 中的一个内置函数，用于获取文件的 MIME 内容类型。

**语法：**

```php
*string* mime_content_type( $file )
```

**参数：**此函数接受单个参数*$file*，该参数指定要查找的 MIME 详细信息的文件路径。

**返回值：**此函数返回 MIME 内容类型，失败时返回 False。

下面的程序演示了 PHP 中的 MIME_CONTENT_TYPE()函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// PHP program to illustrate mime_content_type function

echo mime_content_type('gfg.png') . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
image/png

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
<?php

// PHP program to illustrate 
// mime_content_type function

// Providing and print result of different kind of files 
echo mime_content_type('/home/rajvir/Desktop/gfg.png') . "</br>";
echo mime_content_type('/home/rajvir/Desktop/gfg_Article.html') . "</br>";
echo mime_content_type('/home/rajvir/Downloads/gfg.gif') . "</br>";
echo mime_content_type('/home/rajvir/Desktop/gfg_contribute.txt') . "</br>";
echo mime_content_type('/home/rajvir/Downloads/geeks.ppt') . "</br>";
echo mime_content_type('/home/rajvir/Downloads/geeks.pdf') . "</br>";

?>
```

发帖主题：Re：Колибри0.7.0

```php
image/png
text/plain
image/gif
text/plain
application/vnd.ms-powerpoint
application/pdf

```

**引用：**[http://php.net/manual/en/function.mime-content-type.php](http://php.net/manual/en/function.mime-content-type.php)
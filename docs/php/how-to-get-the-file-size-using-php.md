# 如何用 PHP 获取文件大小？

> 原文:[https://www . geesforgeks . org/如何使用 php 获取文件大小/](https://www.geeksforgeeks.org/how-to-get-the-file-size-using-php/)

在本文中，我们将讨论如何使用 PHP 获取文件大小。PHP 是一种通用脚本语言，适用于网站开发的服务器和客户端脚本语言。为了得到文件大小，我们将使用 file size()函数。

[filesize()函数](https://www.geeksforgeeks.org/php-filesize-function/)以字节为单位返回文件的大小。该函数接受文件名作为参数，并在成功时以字节为单位返回文件大小，在失败时返回 False。

**语法:**

```php
filesize($filename)
```

**参数:**PHP 中的 filesize()函数只接受一个参数，即 ***$filename*** ，该参数指定要检查其大小的文件的文件名。

**示例 1:** 在本例中，我们使用带有文件参数的 filesize()函数，它返回给定文件的大小。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

echo "The File size is: ";

echo filesize("gfg.txt");

?>
```

**输出:**

```php
The File size is: 15
```

**示例 2:** 在本例中，我们使用 filesize()函数，该函数带有一个不存在的文件参数，然后它返回一条错误消息。

## PHP

```php
<?php

echo "The File size is: ";

echo filesize("gfg2.txt");
?>
```

**输出:**

```php
The File size is: 
Warning: filesize(): stat failed for inde1x.php in
C:\xampp\htdocs\gfg.php on line 4
```
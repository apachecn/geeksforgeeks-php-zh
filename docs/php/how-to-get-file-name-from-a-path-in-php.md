# 如何在 PHP 中从路径中获取文件名？

> 原文:[https://www . geesforgeks . org/如何从 php 路径中获取文件名/](https://www.geeksforgeeks.org/how-to-get-file-name-from-a-path-in-php/)

在本文中，我们将看到如何在 PHP 中从路径中获取文件名，并通过示例了解其实现。我们已经给出了完整的路径&我们需要从文件路径中找到文件名。为此，我们将遵循以下 2 种方法:

*   使用 basename()函数
*   使用路径信息( )函数

> **输入:**路径=/testweb/var/www/my website/htdocs/home . PHP
> T3】输出:home.php
> 
> **输入:**路径=/testweb/var/www/my website/htdocs/ABC . txt
> T3】输出: abc.txt

我们将通过例子来理解这两种功能。

**方法一:使用**[**base name()**](https://www.geeksforgeeks.org/php-basename-function/)**功能:**

base name()函数是一个内置函数，如果文件的路径是作为 basename()函数的参数提供的，它将返回文件的基本名称。

**语法:**

```
$filename = basename(path, suffix);
```

路径是指定要检查的路径的必填字段。后缀是指定文件扩展名的可选字段。如果文件名有这个文件扩展名，文件扩展名将不会显示。

**示例**:本示例描述了返回文件基本名称的 basename()函数的使用。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
  $path = "/testweb/var/www/mywebsite/htdocs/home.php";

  $file1 = basename($path);
  $file2 = basename($path, ".php");

  // Show filename with file extension
  echo $file1 . "\n";

  // Show filename without file extension
  echo $file2;
?>
```

**输出:**

```
home.php
home
```

**方法二:使用**[**path info()**](https://www.geeksforgeeks.org/php-pathinfo-function/)**功能:**

pathinfo()是一个内置函数，用于使用关联数组或字符串返回路径信息。，它将创建一个包含我们想要使用的路径部分的数组。

**语法:**

```
$filename = pathinfo(path);
```

**示例**:本示例解释了 pathinfo()函数，该函数将返回关于路径的信息。在这里，我们将使用$filename['basename']，当我们想要访问文件名时。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
  // Path of the file stored under pathinfo
  $myFile = pathinfo('/usr/admin/config/test.php');

  // Show the file name
  echo $myFile['basename'], "\n";
?>
```

**输出:**

```
test.php
```
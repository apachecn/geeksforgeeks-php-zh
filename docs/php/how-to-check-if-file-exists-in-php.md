# 如何在 PHP 中检查文件是否存在？

> 原文:[https://www . geeksforgeeks . org/如何在 php 中检查文件是否存在/](https://www.geeksforgeeks.org/how-to-check-if-file-exists-in-php/)

要检查任何文件是否存在，我们可以使用下面提到的 PHP 函数。要查找文件的存在，我们使用[**file _ exists()**](https://www.geeksforgeeks.org/php-file_exists-function/)**功能。此功能用于检查文件或目录是否存在。**

****语法:****

```php
file_exists( $path )
```

****参数:**这个函数只接受一个参数$path。它指定要检查的文件或目录的路径。**

****返回值:**成功返回真，失败返回假。**

 ****错误和异常:****

*   **如果指定的路径指向不存在的文件，file_exists()函数将返回 False。**
*   **对于大于 2gb 的文件，一些文件系统函数可能会给出意想不到的结果，因为 PHP 的整数类型是带符号的，许多平台使用 32 位整数。**

****示例:**假设存在一个名为“file1.php”的文件。让我们检查文件“file1.php”的存在。**

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```php
<?php

$filename = "file1.php";

if (file_exists($filename)) {
    echo "File exist.";
} else {
    echo "File does not exist.";
}

?>
```

****输出****

```php
File exist.
```
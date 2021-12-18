# 如何使用 PHP 删除文件？

> 原文:[https://www . geesforgeks . org/如何使用-php 删除文件/](https://www.geeksforgeeks.org/how-to-delete-a-file-using-php/)

用 PHP 删除一个文件非常容易。删除文件意味着从目录中完全删除文件，这样文件就不再存在。PHP 有一个 [unlink()函数](https://www.geeksforgeeks.org/php-unlink-function/)，允许删除一个文件。函数接受两个参数*$文件名*和*$上下文*。

**语法:**

```php
unlink( $filename, $context );
```

以下程序说明了上述方法:

**程序 1:** 该程序使用 unlink()函数从目录中删除文件。
假设有一个名为**【gfg . txt】**的文件

```php
<?php
// PHP program to delete a file named gfg.txt 
// using unlike() function 

$file_pointer = "gfg.txt"; 

// Use unlink() function to delete a file 
if (!unlink($file_pointer)) { 
    echo ("$file_pointer cannot be deleted due to an error"); 
} 
else { 
    echo ("$file_pointer has been deleted"); 
} 

?> 
```

**输出:**

```php
gfg.txt has been deleted

```

**程序 2:** 该程序使用 unlink()函数，在使用一些操作后，从文件夹中删除一个文件。

```php
<?php
// PHP program to delete a file named gfg.txt 
// using unlike() function 

$file_pointer = fopen('gfg.txt', 'w+'); 

// writing on a file named gfg.txt 
fwrite($file_pointer, 'A computer science portal for geeks!'); 
fclose($file_pointer);   

// Use unlink() function to delete a file 
if (!unlink($file_pointer)) { 
    echo ("$file_pointer cannot be deleted due to an error"); 
} 
else { 
    echo ("$file_pointer has been deleted"); 
} 

?> 
```

**输出:**

```php
Warning: unlink() expects parameter 1 to be a valid path, resource
given in C:\xampp\htdocs\server.php on line 12
Resource id #3 cannot be deleted due to an error

```

**注意:**如果文件不存在，将显示错误。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
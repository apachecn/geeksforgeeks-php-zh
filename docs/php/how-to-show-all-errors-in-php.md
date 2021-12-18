# 如何显示 PHP 中的所有错误？

> 原文:[https://www . geesforgeks . org/how-show-all-in-errors-PHP/](https://www.geeksforgeeks.org/how-to-show-all-errors-in-php/)

我们可以使用 ***错误报告()*** 功能显示 PHP 中的所有错误。它根据提供的级别在运行时设置 ***错误报告*** 指令。如果没有提供级别，它将返回当前的错误报告级别。**错误报告(E_ALL)** 级别代表所有错误、警告、通知等。

**PHP 代码:**如果级别设置为零，即使包含不可用的文件，也不会报告错误。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
   //setting error reporting to zero
  error_reporting(0);
  //including a file that is not present
  include(gfg.php);
?>
```

**输出:**

```
No output
No error is reported
```

**PHP 代码:**

当级别设置为 E_ALL 时，将报告所有错误，包括所有警告和通知。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    //setting error reporting to all errors
  error_reporting(E_ALL);
   //including a file that is not present
  include(gfg.php);
?>
```

**输出:**

> PHP 通知:在第 5 行
> PHP 通知:在/home/36649711d 0 ef 1764 ba 295676144 de 779 . PHP 中使用未定义常量 gfg–在/home/36649711d 0 ef 1764 ba 295676144 de 779 . PHP 中使用未定义常量 PHP–在/home/36649711d 0 ef 1764 ba 295676144 de 779 . PHP 第 5 行
> PHP 警告:include(gfgphp):未能

参考文献:[https://www.php.net/manual/en/function.error-reporting.php](https://www.php.net/manual/en/function.error-reporting.php)[https://www.geeksforgeeks.org/php-types-of-errors/](https://www.geeksforgeeks.org/php-types-of-errors/)
# PHP 中如何检查一个变量是否为空？

> 原文:[https://www . geesforgeks . org/如何在 php 中检查变量是否为空/](https://www.geeksforgeeks.org/how-to-check-whether-a-variable-is-null-in-php/)

我们给了一个变量，任务是检查给定变量的值是否为空，并使用 PHP 返回一个布尔值。为了检查一个变量是否为空，我们使用 [is_null()函数](https://www.geeksforgeeks.org/php-is_null-function/)。如果变量不存储任何值，则被认为是空的。如果变量$var 的值为空，则返回真，否则返回假。

**语法**

```
boolean is_null( $var )
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP Program to check whether
// a variable is null or not?

$var1 = NULL;
$var2 = "\0"; // "\0" means null character
$var3 = "NULL";

// $var1 has NULL value, so always give TRUE
is_null($var1) ? print_r("True\n") : print_r("False\n");

// $var2 has '\0' value which consider as null in
// c and c++ but here taken as string, gives FALSE
is_null($var2) ? print_r("True\n") : print_r("False\n");

// $var3 has NULL string value so it will false
is_null($var3) ? print_r("True\n") : print_r("False\n");

?>
```

**输出:**

```
True
False
False
```
# 在 PHP 中是 _ null($ x)vs $ x = = = null

> 原文:[https://www.geeksforgeeks.org/is_nullx-vs-x-null-in-php/](https://www.geeksforgeeks.org/is_nullx-vs-x-null-in-php/)

**[为 _null()函数](https://www.geeksforgeeks.org/php-is_null-function/)**

这个 is_null()函数是 PHP 中的一个内置函数，用来查找一个变量是否为 null。如果给定变量为空，则返回真，否则返回假。

**语法:**

```
*bool* is_null( $var )
```

**例 1:**

```
<?php
// PHP program to illustrate
// is_null() function

// Declare variable and initialize it
$x = NULL;
$y = 15;

// Use is_null() function and 
// display the result
var_dump(is_null($x));

var_dump(is_null($y));

?>
```

**输出:**

```
bool(true)
bool(false)

```
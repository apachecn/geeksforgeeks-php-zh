# 如何在 PHP 中从数组创建逗号分隔列表？

> 原文:[https://www . geesforgeks . org/how-create-逗号分隔列表-来自 php 中的数组/](https://www.geeksforgeeks.org/how-to-create-comma-separated-list-from-array-in-php/)

使用 **[内爆()功能](https://www.geeksforgeeks.org/php-implode-function/)** 可以创建逗号分隔列表。内爆()是 PHP 中的内置函数，用于连接数组的元素。内爆()是 PHP | join()函数的别名，工作原理与 join()函数完全相同。
如果我们有一个元素数组，我们可以使用内爆()函数将它们连接起来形成一个字符串。我们基本上是用字符串连接数组元素。就像 join()函数一样，内爆()函数也返回一个由数组元素组成的字符串。

**语法:**

```php
*string* implode( separator, array )

```

**返回类型:**内爆()函数的返回类型为 string。它将返回由数组元素组成的连接字符串。

**示例 1:** 本示例向数组元素添加逗号分隔符。

```php
<?php

// Declare an array and initialize it
$Array = array( "GFG1", "GFG2", "GFG3" );

// Display the array elements
print_r($Array);

// Use implode() function to join
// comma in the array
$List = implode(', ', $Array);

// Display the comma separated list
print_r($List);

?>
```

**Output:**

```php
Array
(
    [0] => GFG1
    [1] => GFG2
    [2] => GFG3
)
GFG1, GFG2, GFG3

```
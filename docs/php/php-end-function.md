# PHP end()函数

> Original: [https://www.geeksforgeeks.org/php-end-function/](https://www.geeksforgeeks.org/php-end-function/)

在本文中，我们将了解如何使用 PHP 中的 end()函数获取数组中的最后一个元素，并通过示例了解它们的实现。

函数**end()**是 PHP 中的内置函数，用于查找给定数组的最后一个元素。 函数的作用是：将数组的内部指针改为指向最后一个元素，并返回最后一个元素的值。

**语法：**

```
end($array)
```

**参数：**此函数接受单个参数*$array*。 它是我们想要找到的最后一个元素的数组。

**返回值**：如果成功，则返回数组最后一个元素的值；否则，如果数组为空，则返回 FALSE。

请考虑以下示例。

```
Input: array('Ram', 'Shita', 'Geeta')
Output: Geeta
Explanation: Here, the input array contain many elements
but output is Geeta i.e, last element of the array 
as the end() function returns the last element of an array.
```

**示例 1**：下面的示例说明了 PHP 中的 end()函数。

## PHP

```
<?php

  // Input array
  $arr = array('Ram', 'Shita', 'Geeta');

  // end function print the last
  // element of the array.
  echo end($arr);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2**：此示例说明从数组中检索最后一个元素。

## PHP

```
<?php

  // Input array
  $arr = array('1', '3', 'P');

  // end function print the last
  // element of the array.
  echo end($arr)."\n";

  // end() updates the internal pointer
  // to point to last element as the
  // current() function will now also
  // return last element
  echo current($arr);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.end.php](http://php.net/manual/en/function.end.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
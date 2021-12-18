# 如何在 PHP 中声明一个全局变量？

> 原文:[https://www . geesforgeks . org/如何在 php 中声明一个全局变量/](https://www.geeksforgeeks.org/how-to-declare-a-global-variable-in-php/)

全局变量是指在函数外部定义的任何变量。全局变量可以从脚本的任何部分访问，即函数的内部和外部。因此，全局变量可以像其他变量一样声明，但它必须在函数定义之外声明。

**语法:**

```
$variable_name = data;
```

下面的程序说明了如何声明全局变量。

**例 1:**

```
<?php
// Demonstrate how to declare global variable

// Declaring global variable
$x = "Geeks";
$y = "for";
$z = "Geeks";

// Display value
// Concatenating String
echo $x.$y.$z;

?>
```

**输出:**

```
GeeksforGeeks

```
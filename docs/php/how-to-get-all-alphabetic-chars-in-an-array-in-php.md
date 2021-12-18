# 如何在 PHP 中获取数组中的所有字母字符？

> 原文:[https://www . geesforgeks . org/如何获取 php 数组中的所有字母字符/](https://www.geeksforgeeks.org/how-to-get-all-alphabetic-chars-in-an-array-in-php/)

数组中的所有字母字符都可以通过在 PHP 中使用 chr()、range()以及 for 和 foreach 循环来实现。要将数组元素显示为输出，我们可以使用 echo、print_r()和 var_dump()函数。

**[使用 range()函数](https://www.geeksforgeeks.org/php-range-function/) :** 该函数用于创建给定范围内(从低到高)的任意类型元素(如整数、字母)的数组，即列表的第一个元素被视为低，最后一个元素被视为高。如果范围是从 A 到 Z，即范围(A，Z)，它将返回一个字母数组。

**语法:**

```
*array* range( *mixed* first, *mixed* second, *number* steps )
```

**示例 1:** 以下示例说明如何使用 range()函数显示所有字母字符的数组。

```
<?php 

// Loop to take values from given range
// and display the range elements
foreach( range('A', 'Z') as $elements) {

    // Display all alphabetic elements
    // one after another
    echo $elements . ", ";
}

?>
```

**输出:**

```
A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z,

```
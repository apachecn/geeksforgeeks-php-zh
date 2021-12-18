# PHP 中如何限制字符串长度？

> 原文:[https://www . geesforgeks . org/如何在 php 中限制字符串长度/](https://www.geeksforgeeks.org/how-to-limit-string-length-in-php/)

字符串是 PHP 中的一系列字符。在 PHP 中，可以使用各种内置函数来限制字符串的长度，其中可以限制字符串字符数。

**方法 1(用于循环):**str _ split()函数可用于将指定的字符串转换为数组对象。数组元素是存储在单个索引中的单个字符。

```
str_split($string)
```

**参数:**

*   **$ string-** Split strings into arrays.

**示例:**在数组对象上执行循环迭代，直到达到所需的长度。显示字符，直到长度等于所需的字符数。

## PHP

```
<?php
    $string = "Geeks for geeks is fun";
    echo("Original String : ");

    echo($string . "\n");
    echo("Modified String : ");

    $arr = str_split($string);

    for($i = 0; $i < 10; $i++) {
        print($arr[$i]);
    }
?>
```

**输出**

```
Original String : Geeks for geeks is fun
Modified String : Geeks for 
```
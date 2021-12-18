# PHP 中如何从字符串中提取数字？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中提取数字/](https://www.geeksforgeeks.org/how-to-extract-numbers-from-a-string-in-php/)

本文的目的是使用 PHP 从字符串中提取数字。

**进场:**

我们可以使用 [**preg_replace()**](https://www.geeksforgeeks.org/php-preg_replace-function/) 函数从字符串中提取数字。

*   **/[^0-9]/** 模式用于在字符串中查找数字为*整数*(参见例 1 )
*   **/[^0-9\.]/** 模式用于查找字符串中的双精度数字(参见示例 2)

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    $string = '$ 90,000,000.0098';
    echo preg_replace("/[^0-9]/", '', $string);
    echo "\n<br/>";

    $string2 = '$ 90,000,000.0098';
    echo preg_replace("/[^0-9\.]/", '', $string2);
?>
```

**Output**

```
900000000098
90000000.0098
```

**例 2:** 从字符串中提取数字的完整代码如下

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    $string = '$ 90,000,000.0098';
    echo preg_replace("/[^0-9]/", '', $string);
    echo "\n<br/>";

    $string2 = '$ 90,000,000.0098';
    echo preg_replace("/[^0-9\.]/", '', $string2);
    echo "\n<br/>";

    $string3 = 'Jack has 10 red and 14 blue balls';
    echo preg_replace("/[^0-9]/", '', $string3);
    echo "\n";
?>
```

**Output**

```
900000000098
90000000.0098
1014
```
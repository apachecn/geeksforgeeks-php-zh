# 在 PHP 中用前导零格式化一个数字

> 原文:[https://www . geesforgeks . org/format-一个带前导零的数字-php/](https://www.geeksforgeeks.org/format-a-number-with-leading-zeros-in-php/)

在编写代码时，我们经常会遇到需要填充数字/字符串并使它们具有默认长度的情况。在本文中，我们将学习如何在 PHP 中用前导零填充数字。
为了更好地理解任务，这里举几个例子。
**例:**

```
Input :1234567
Output :01234567

Input :1234
Output :00001234
```

有许多方法可以填充字符串格式的前导零。但是在字符串的情况下，完成任务的最好方法是使用 [sprintf](http://php.net/manual/en/function.sprintf.php) 函数，也可以使用 [substr()](https://www.php.net/manual/en/function.substr.php) 函数。

*   [sprintf()](http://php.net/manual/en/function.sprintf.php) 功能
*   [substr()](https://www.php.net/manual/en/function.substr.php) 函数

**使用 sprintf()函数:**sprintf()函数用于返回格式化的字符串。
**语法:**

```
sprintf(format, $variable)
// Returns the variable formated according to the format provided. 
```

*   **示例 1:** 本示例使用 sprintf()函数显示带前导零的数字。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$var = 1234567;
echo sprintf('%08d', $var);
?>
```

*   **输出:**

```
01234567
```

*   **示例 2:** 本示例使用 sprintf()函数显示带前导零的负数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$var1 = -10;
$var2 = 10;
echo sprintf('%04s', $var1) . "\n";
echo sprintf('%04s', $var2);
?>
```

*   **输出:**

```
0-10
0010
```

*   在上面的例子中，我们试图将数字格式化为字符串，并打乱了负数。但如果我们使用“%d”而不是“%s”来格式化数字，情况就不是这样了。
*   **例 3:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$var1 = -10;
$var2 = 10;
echo sprintf('%04d', $var1) . "\n";
echo sprintf('%04d', $var2);
?>
```

*   **输出:**

```
-010
0010
```

**使用 substr()函数:**该函数用于返回字符串的一部分。
**语法:**

```
substr( string $string , int $start, int $length )
// Returns the portion of string that define at start and length of the parameter. 
```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$num = 123;
$str_length = 4;

// Left padding if number < $str_length
$str = substr("0000{$num}", -$str_length);
echo sprintf($str);
?>
```

**输出:**

```
0123
```
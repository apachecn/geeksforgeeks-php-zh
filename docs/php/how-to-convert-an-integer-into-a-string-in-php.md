# 如何在 PHP 中将整数转换成字符串？

> 原文:[https://www . geesforgeks . org/如何在 php 中将整数转换为字符串/](https://www.geeksforgeeks.org/how-to-convert-an-integer-into-a-string-in-php/)

函数的作用是:在 PHP 中将一个整数转换成一个字符串。还有许多其他方法可以将整数转换为字符串。

在这篇文章中，我们将学习许多方法。

**方法:**

*   Use **strval ()** function.
*   Use inline variable resolution.
*   Use explicit casting.

**方法 1:** 使用 **strval()** 功能。

**注意:****strval()**函数是 PHP 中的内置函数，用于将任何标量值(字符串、整数或双精度)转换为字符串。我们不能在数组或对象上使用 strval()，如果应用的话，这个函数只返回被转换的值的类型名。

**语法:**

```php
strval( $variable ) 
```

**返回值:**这个函数返回一个字符串。该字符串是通过将传递给它的变量值作为参数进行类型转换而生成的。

**示例:**

## PHP

```php
<?php

$var_name = 2;

// converts integer into string
$str =  strval($var_name);

// prints the value of above variable as a string
echo "Welcome $str GeeksforGeeks";

?>
```

**输出**

```php
Welcome 2 GeeksforGeeks
```

**方法 2:** 使用**内联**变量解析。

**注意:**当在字符串内部使用 Integer 时，那么 Integer 首先被转换为字符串，然后作为字符串打印。

**语法:**

```php
$integer = 2;
echo "$integer";
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$var_name = 2;

// prints the value of above variable
// as a string
echo "Welcome $var_name GeeksforGeeks";

?>
```

**Output**

```php
Welcome 2 GeeksforGeeks
```

**方法 3:** 使用显式铸造。

**注意:**显式强制转换是数据类型的显式转换，因为用户明确定义了他想要强制转换的数据类型。我们将整数转换成字符串。

**语法:**

```php
$str = (string)$var_name
```

**示例:**

## PHP

```php
<?php

$var_name = 2;

//Typecasting Integer into string
$str = (string)$var_name;

// prints the value of above variable as a string
echo "Welcome $str GeeksforGeeks";

?>
```

**输出**

```php
Welcome 2 GeeksforGeeks
```
# PHP 中如何将 String 转换为 Float？

> 原文:[https://www . geesforgeks . org/如何将字符串转换为 php 中的浮点数/](https://www.geeksforgeeks.org/how-to-convert-string-to-float-in-php/)

PHP 中的字符串可以非常容易地转换为浮点型。在大多数用例中，它不是必需的，因为 PHP 做隐式类型转换。在 PHP 中将字符串转换成数字的方法有很多，下面讨论其中的一些:

**方法:**

*   使用 **floatval()** 功能。
*   使用类型转换。
*   使用 **number_format()** 功能。

**方法 1:** 使用 [**floatval()**](https://www.geeksforgeeks.org/how-to-convert-a-string-into-number-in-php/) 功能。

**注意:****float val()**函数可用于将字符串转换为浮点值。

**语法:**

```php
$floatvar = floatval($stringvar)
```

**返回值:**该函数返回一个*浮点数*。这个浮点数是通过类型转换作为参数传递给它的变量值而生成的。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // Number in string format
  $stringvar = "1000.314";

  // converts string into float
  $floatvar =  floatval($stringvar);

  // prints the value of above variable as a float
  echo "Converted float = ".$floatvar;

?>
```

**输出:**

```php
Converted float = 1000.314
```

**方法 2:** 使用类型转换。

**注意:** Typecasting 是数据类型的显式转换，因为用户明确定义了他想要在其中进行类型转换的数据类型。我们将字符串转换为浮点。

**语法:**

```php
$floatvar = (float)$stringvar
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Number in string format
$stringvar = "1000.314";

// converts string into float
$floatvar =  (float)$stringvar;

// prints the value of above variable as a float
echo "Converted float = ".$floatvar;

?>
```

**输出:**

```php
Converted float = 1000.314
```

**方法三:**使用 [**number_format()**](https://www.geeksforgeeks.org/php-number_format-function/) 功能。

**注意:****number _ format()**函数是 PHP 中的一个内置函数，用于格式化成组的千位数字。它在成功时返回格式化的数字，否则在失败时给出 E_WARNING。

**语法:**

```php
string number_format( $number, $decimals, $decimalpoint, $sep )
```

**返回值:**成功则返回一个格式化的数字，否则失败则给出 E_WARNING。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Number in string format
$stringvar = "1000.3145635";

// converts  string into float with 6 decimals
$floatvar =  number_format($stringvar, 6);

// prints the value of above variable as a string
echo "Converted float = ".$floatvar;

?>
```

**输出:**

```php
Converted float = 1000.314564
```
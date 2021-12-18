# PHP|strrev()函数

> Original: [https://www.geeksforgeeks.org/php-strrev-function/](https://www.geeksforgeeks.org/php-strrev-function/)

反转字符串是最基本的字符串操作之一，开发人员和程序员非常频繁地使用它。 PHP 附带了一个用于反转字符串的内置函数。

**strrev()**函数是 PHP 中的内置函数，用于反转字符串。 此函数不会对作为参数传递给它的原始字符串进行任何更改。

**语法：**

```
*string* strrev($inpString)
```

**参数：**此函数接受单个参数*$inpString*。 此参数是一个字符串，它指定要反转的字符串。 如果传递给它的是数字而不是字符串，它也会反转该数字。

**返回值：**strrev()函数返回反转的字符串或数字。 它不会对参数中传递的原始字符串或数字进行任何更改。

例如：

```
Input : $string = "geeks" 
Output : skeeg 

Input : $string = 143 
Output : 341 
```

下面的程序演示了 PHP 中的 strrev()函数：

**程序 1：**传递字符串时演示 strrev()函数的 PHP 程序。

## PHP

```
<?php
// PHP program to demonstrate the
// strrev() function when a string is passed

$str = "geeks";

// prints the reversed string
echo strrev($str);
?>
```

产出：

```
skeeg
```

**程序 2：**PHP 程序，用于在传递数字时演示 strrev()函数。

## PHP

```
<?php
// PHP program to demonstrate the
// strrev() function when a number is passed

// passing number instead of string
$num = 134;

// prints the reversed number
echo strrev($num);
?>
```

产出：

```
431
```

**参考**：
[http://php.net/manual/en/function.strrev.php](http://php.net/manual/en/function.strrev.php)
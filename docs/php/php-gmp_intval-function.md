# PHP|gmp_intval()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_intval-function/](https://www.geeksforgeeks.org/php-gmp_intval-function/)

Gmp_intval()是 PHP 中的一个内置函数，用于将 GMP 数字转换为整数。 这里，GMP 指的是[GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)，它代表大数。
**语法：**

```php
int gmp_intval ( $num )
```

**参数：**该函数接受单个参数*$num*，该参数是一个 GMP 编号并返回其整数值。 此参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
**返回值：**此函数返回给定 GMP 编号的整数值*$Num*
示例：

```php
Input : $num = "2147483647"
Output :  2147483647

Input : $num = "12"
Output :  12
```

**注意：**如果数字字符串作为整数传递，则返回相同的整数(高于 PHP 整数限制除外)。 但如果传递 GMP 数字，它将返回 GMP 数字的整数值。下面的程序说明了**gmp_intval()**函数的用法：
**程序 1：**下面的程序演示了将数字字符串作为参数传递时 gmp_intval()函数的工作方式。

## PHP

```php
<?php
// PHP program to demonstrate the gmp_intval()
// function when argument is passed

$x = gmp_intval("2147") . "\n";

// prints integer value of a gmp number

// it returns the same numeric string in integer form
echo gmp_strval($x) . "\n";
?>
```

输出：0

```php
2147
```

**程序 2：**下面的程序演示了将 gmp 编号作为参数传递时 gmp_intval()的工作方式。

## PHP

```php
<?php
// PHP program to demonstrate the gmp_intval() function
// when GMP number is passed as an argument

// arguments as GMP numbers
$num = gmp_init("1111", 2); // num initialisation = 12

// integer value of GMP number 12 is 12
$x = gmp_intval($num);

// prints the integer value of a gmp number
// gmp_strval converts GMP number to string
// representation in given base(default 10).
echo gmp_strval($x) . "\n";
?>
```

输出：0

```php
7
```

**引用：**
[http://php.net/manual/en/function.gmp-intval.php](http://php.net/manual/en/function.gmp-intval.php)
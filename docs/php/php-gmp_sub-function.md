# PHP|gmp_sub()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_sub-function/](https://www.geeksforgeeks.org/php-gmp_sub-function/)

Gmp_sub()是 PHP 中的一个内置函数，它返回两个 GMP 数字的减法。([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)

**语法：**

```php
gmp_sub($num1, $num2)
```

**参数：**此函数接受两个 GMP 编号*$num1*和*$num2*作为上述语法中显示的强制参数。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回两个数字$num1 和$num2 的减法。

例如：

```php
Input : $num1=5 , $num2=10
Output : -5 

Input : $num1=7 , $num2=1
Output : 6 

```

以下程序说明了**gmp_sub()**函数：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时，gmp_sub()函数的工作原理。

```php
<?php
// PHP program to subtract two 
// two numbers 

// GMP number as arguments 
$num1 = gmp_init("101", 2);
$num2 = gmp_init("1010", 2); 

// 5-10 = -5 
$sub = gmp_sub($num1, $num2); 

// gmp_strval converts GMP number to string 
// representation in given base(default 10).
echo gmp_strval($sub, 2);
?>
```

产出：

```php
-101
```

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_sub()的工作方式。

```php
<?php
// PHP program to subtract two 
// two numbers 

// numeric strings number as arguments 
$num1 = "7";
$num2 = "1";

// 7-1 = 6
$sub = gmp_sub($num1, $num2); 

echo $sub;
?>
```

产出：

```php
6
```

**引用：**
[http://php.net/manual/en/function.gmp-sub.php](http://php.net/manual/en/function.gmp-sub.php)
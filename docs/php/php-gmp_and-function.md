# PHP|gmp_and()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_and-function/](https://www.geeksforgeeks.org/php-gmp_and-function/)

Gmp_and()是 PHP 中的一个内置函数，用于计算两个 GMP 数字的位**和**([GNU Multiple Precision：对于大数](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))。

**语法：**

```php
gmp_and($num1, $num2)
```

**参数：**此函数接受两个 GMP 编号$num1、$num2 作为必选参数，如上面的语法所示。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，以便可以将这些字符串转换为数字。

**返回值：**此函数返回按位传递的 GMP 编号以及作为参数传递给它的 GMP 编号。

例如：

```php
Input : gmp_and("4", "2")
Output : 0

Input : gmp_and("9", "10")
Output : 8

```

下面的程序演示了 PHP 中的 gmp_and()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，计算 GMP 编号的位与运算的程序。

```php
<?php
// PHP program to calculate the bitwise AND
// GMP numbers passed as arguments 

// strings as GMP numbers
$num1 = "10";
$num2 = "9";

// calculate the bitwise AND of $num1 and $num2
$res = gmp_and($num1, $num2);

echo $res;

?>
```

产出：

```php
8
```

**程序 2：**当 GMP 编号作为参数传递时，计算 GMP 编号的位与运算的程序。

```php
<?php
// PHP program to calculate the bitwise AND
// GMP numbers passed as arguments 

// creating GMP numbers using gmp_init()
$num1 = gmp_init(4);
$num2 = gmp_init(2);

//calculate the bitwise AND of $num1 and $num2
$res = gmp_and($num1, $num2);
echo $res;

?>
```

产出：

```php
0

```

**引用：**
[http://php.net/manual/en/function.gmp-and.php](http://php.net/manual/en/function.gmp-and.php)
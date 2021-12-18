# PHP|gmp_sign()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_sign-function/](https://www.geeksforgeeks.org/php-gmp_sign-function/)

Gmp_sign()是 PHP 中的一个内置函数，用于检查给定 GMP 编号的符号([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```php
gmp_sign($num)
```

**参数：**此函数接受一个 GMP 编号*$num*作为上述语法中显示的强制参数。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**该函数检查给定数字*$num*的符号，并根据数字返回三个值，如下所述：

*   **返回 1**-$num 为正数
*   **返回-1**-$num 为负数
*   **返回 0**-$num 为零

例如：

```php
Input : $num=9
Output : 1 

Input : $num=-8
Output : -1 

Input : $num=0
Output : 0 

```

以下程序说明了 gmp_sign()函数：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时 gmp_sign()函数的工作方式。

```php
<?php
// PHP program to check the sign 
// of a number 

// GMP arguments 
// negative 
$num1 = gmp_init("-101", 2);

// positive
$num2 = gmp_init("1010", 2); 

// zero
$num3 = gmp_init("0", 2); 

// prints -1 as negative
echo gmp_sign($num1)."\n"; 

// prints +1 as negative
echo gmp_sign($num2)."\n";  

// prints 0 as 0
echo gmp_sign($num3)."\n"; 

?>
```

产出：

```php
-1
1
0

```

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_sign()的工作方式。

```php
<?php
// PHP program to check the sign 
// of a number 

// numeric arguments 

// negative 
$num1 = -9;

// positive
$num2 = 8;

// zero
$num3 = 0;

// prints -1 as negative
echo gmp_sign($num1)."\n"; 

// prints +1 as negative
echo gmp_sign($num2)."\n";  

// prints 0 as 0
echo gmp_sign($num3)."\n"; 

?>
```

产出：

```php
-1
1
0
```

**引用：**
[http://php.net/manual/en/function.gmp-sign.php](http://php.net/manual/en/function.gmp-sign.php)
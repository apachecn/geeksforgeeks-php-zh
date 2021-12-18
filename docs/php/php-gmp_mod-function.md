# PHP|gmp_mod()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_mod-function/](https://www.geeksforgeeks.org/php-gmp_mod-function/)

Gmp_mod()是 PHP 中的一个内置函数，用于查找 GMP 编号([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)与另一个 GMP 编号*$d*的乘积，其中忽略了*$d*的符号。

**语法：**

```php
gmp_mod ( $num, $d )
```

**参数：**该函数接受两个 GMP 编号*$num*和*$d*作为必选参数，如上面的语法所示。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递多个数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回的 GMP 编号等于(**$num%$d**)。

例如：

```php
Input : $num="8" $d="3" 
Output :  2

Input : $num="10" $d="4"
Output :  2

```

以下程序说明了 gmp_mod()函数：

**程序 1：**下面的程序演示了将数字字符串作为参数传递时 gmp_mod()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_mod() function

// arguments as numeric strings 
$mod = gmp_mod("8", "3"); 

// prints the calculated modulous
echo gmp_strval($mod) . "\n";  
?>
```

产出：

```php
2
```

**程序 2：**下面的程序演示了当 GMP 编号作为参数传递时 gmp_mod()的工作方式。

```php
<?php
// PHP program to demonstrate the gmp_mod function

// arguments as GMP numbers

$num = gmp_init("1010", 2); // num = 10 
$d = gmp_init("100", 2);  // d = 4

$mod = gmp_mod($num, $d);

// prints the calculated modulous
// gmp_strval converts GMP number to string 
// representation in given base(default 10).
echo gmp_strval($mod) . "\n";  
?>
```

产出：

```php
2
```

**引用：**
[http://php.net/manual/en/function.gmp-mod.php](http://php.net/manual/en/function.gmp-mod.php)
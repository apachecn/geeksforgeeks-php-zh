# PHP|gmp_div_q()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_div_q-function/](https://www.geeksforgeeks.org/php-gmp_div_q-function/)

Gmp_div_q()是 PHP 中的一个内置函数，用于执行 GMP 编号的除法([GNU Multiple Precision：for Large Number](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))。

**语法：**

```php
gmp_div_q($num1, $num2)
```

**参数：**此函数接受 GMP 编号、$num1 和$num2 作为必选参数，如上面的语法所示。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，以便可以将这些字符串转换为数字。

**返回值：**此函数返回一个 GMP 编号，它是$num1 除以$num2 时的商。 该函数根据$num1 和$num2 的值返回正、负或零。

例如：

```php
Input : gmp_div_q("256", "16")
Output : 16

Input : gmp_div_q("188", "4")
Output : 47

```

以下程序说明了 PHP 中的 gmp_div_q()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，执行 GMP 编号除法的程序。

```php
<?php
// PHP program to perform division of
// GMP numbers passed as arguments 

// strings as GMP numbers 
$num1 = "-6";
$num2 = "2";

// caluates the quotient when
// $num1 is divided by $num2
$quo = gmp_div_q($num1, $num2);

echo $quo;
?>
```

产出：

```php
-3

```

**程序 2：**当 GMP 编号作为参数传递时执行 GMP 编号除法的程序。

```php
<?php
// PHP program to perform the division of
// GMP numbers

// creating GMP numbers using gmp_init()
$num1 = gmp_init(289);
$num2 = gmp_init(17);

// caluates the quotient when
// $num1 is divided by $num2
$quo = gmp_div_q($num1, $num2);

echo $quo;
?>
```

产出：

```php
17

```

**程序 3：**当 GMP 编号作为参数传递时执行 GMP 编号除法的程序。

```php
<?php
// PHP program to perform the division of
// GMP numbers

// creating GMP numbers using gmp_init()
$num1 = gmp_init(3);
$num2 = gmp_init(4);

// caluates the quotient when
// $num1 is divided by $num2
$quo = gmp_div_q($num1, $num2);

echo $quo;
?>
```

产出：

```php
0
```

**引用：**
[http://php.net/manual/en/function.gmp-div-q.php](http://php.net/manual/en/function.gmp-div-q.php)
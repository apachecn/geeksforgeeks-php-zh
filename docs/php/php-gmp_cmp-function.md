# PHP|gmp_cmp()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_cmp-function/](https://www.geeksforgeeks.org/php-gmp_cmp-function/)

Gmp()是 PHP 中的一个内置函数，用于比较两个 GMP 数字([GNU Multiple Precision：for Large Number](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))。

**语法：**

```php
gmp_cmp($num1, $num2)
```

**参数：**此函数接受两个 GMP 编号*$num1*和*$num2*作为必选参数，如上面的语法所示进行比较。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，以便可以将这些字符串转换为数字。

**返回值：**如果$num1>$num2，函数返回“1”；如果$num1 等于$num2，则返回“0”；如果$num1<$num2，则返回“-1”。

例如：

```php
Input : gmp_cmp("1234", "1236")
Output : -1

Input : gmp_cmp("3569", "3569")
Output : 0

```

以下程序说明了 PHP 中的 gmp_cmp()函数：

**程序 1：**当两个 GMP 编号作为数字字符串传递时，比较它们的程序。

```php
<?php
// PHP program to compare two
// GMP numbers passed as arguments 

// strings as GMP numbers 
$num1 = "12356";
$num2 = "12356";

// compares the two numbers and
// gives the result "0" as both are equal 
$res = gmp_cmp($num1, $num2);

echo $res;

?>
```

产出：

```php
0
```

**程序 2：**当两个 GMP 编号作为参数传递时，比较两个 GMP 编号的程序。

```php
<?php

// PHP program to compare two
// GMP numbers passed as arguments 

// creating GMP numbers using gmp_init()
$num1 = gmp_init(12355);
$num2 = gmp_init(12356);

// compares these two numbers and
// gives the result "-1" as $num1 < $num2
$res = gmp_cmp($num1, $num2);

echo $res;
?>
```

产出：

```php
-1

```

**引用：**
[http://php.net/manual/en/function.gmp-cmp.php](http://php.net/manual/en/function.gmp-cmp.php)
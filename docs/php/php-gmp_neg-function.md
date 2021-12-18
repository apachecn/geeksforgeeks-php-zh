# PHP|gmp_neg()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_neg-function/](https://www.geeksforgeeks.org/php-gmp_neg-function/)

gmp_neg()函数是 PHP 中的一个内置函数，它返回 GMP 编号[(GNU 倍数精度)](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)的负值。

**语法：**

```php
gmp_neg( $num  )
```

**参数：**该函数只接受一个强制参数**$num**，该参数可以是 PHP 5.5 中的 GMP 编号资源，也可以是 PHP 5.6 及更高版本中的 GMP 对象，或者可以将数字字符串传递给该函数，前提是可以将这些字符串转换为数字。

**返回值：**此函数返回 GMP 编号(在 PHP 5.5 和更早版本中)或 GMP 对象(在 PHP 5.6 和更高版本中)，其值为**$num**的负值。

**示例：**

```php
Input : $num = 255 
Output : -255

Input : $num = 128 
Output : -128

```

以下程序将演示 gmp_neg()函数：

**程序 1**：

```php
<?php
//PHP program to illustrate
//gmp_neg() function

$num = gmp_init("255");

$num1 = gmp_neg($num);

echo gmp_strval($num1);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
-255
```

**程序 2**：

```php
<?php
//PHP program to illustrate
//gmp_neg() function

$num = gmp_init("314567128");

$num1 = gmp_neg($num);

echo gmp_strval($num1);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
-314567128
```

**引用：**[http://php.net/manual/en/function.gmp-neg.php](http://php.net/manual/en/function.gmp-neg.php)
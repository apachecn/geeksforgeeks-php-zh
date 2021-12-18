# PHP|gmp_gcd()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_gcd-function/](https://www.geeksforgeeks.org/php-gmp_gcd-function/)

**GMP_GCD()**是 PHP 中的一个内置函数，用于计算 2[GMP](http://php.net/manual/en/class.gmp.php)数字的**GCD**([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```php
gmp_gcd ( $num1, $num2 )

```

**参数：**此函数接受两个 GMP 编号$num1 和$num2 作为参数。 此函数计算这两个数字的 GCD。

**返回值：**此函数返回正的**[gmp](http://php.net/manual/en/class.gmp.php)**数字，它是$num1 和$num2 的 GCD。

例如：

```php
Input : gmp_gcd("12", "21")
Output : 3

Input : gmp_gcd("15", "30")
Output : 15

```

**说明：**在上例中**gmp_gcd()**函数计算 num1 和 num2 的最大公约数。 即使输入操作数中的一个或两个都为负，结果也始终为正。

下面的程序演示了 PHP 中的**gmp_gcd()**函数。

**程序 1：**

```php
<?php

$gcd = gmp_gcd("12", "21");
echo gmp_strval($gcd) . "\n";

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
3
```

**程序 2：**

```php
<?php

$gcd = gmp_gcd("15", "30");
echo gmp_strval($gcd) . "\n";

?>
```

发帖主题：Re：Колибри0.7.0

```php
15
```

**引用：**
[http://php.net/manual/en/function.gmp-gcd.php](http://php.net/manual/en/function.gmp-gcd.php)
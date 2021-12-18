# PHP|gmp_mul()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_mul-for-multiply-large-numbers/](https://www.geeksforgeeks.org/php-gmp_mul-for-multiply-large-numbers/)

PHP 中的 gmp_mul()函数是一个内置函数，用于将两个 GMP 数字相乘([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```php
GMP gmp_mul ( GMP $num1, GMP $num2 )
```

**参数：**此函数接受两个 GMP 编号。 如以上语法所示，为必选参数。 它们可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以是数字字符串，前提是可以将后者转换为数字。 此函数将这两个数字相乘并返回。

**返回值：**此函数返回一个 GMP 编号，它是作为参数传递的两个数字的乘积。

例如：

```php
Input : num1 = "123456789"
        num2 = "987654321"
Output: 121932631112635269

Input : num1 = "9999999"
        num2 = "99999"
Output: 999989900001

```

以下程序说明了 PHP 中的 gmp_mul()函数：

**程序 1：**

```php
<?php
$mul = gmp_mul("562817", "713645");
echo gmp_strval($mul);
?>
```

产出：

```php
401651537965
```

**程序 2：**

```php
<?php
$mul = gmp_mul("123456789", "987654321");
echo gmp_strval($mul); 
?>
```

输出：
**相关文章：**

*   [PHP|gmp_neg()函数](https://www.geeksforgeeks.org/php-gmp_neg-function/)
*   [PHP|gmp_clrbit()函数](https://www.geeksforgeeks.org/php-gmp_clrbit-function/)
*   [PHP|GMP 标签函数](https://www.geeksforgeeks.org/tag/php-gmp/)

```php
121932631112635269
```

**引用：**[http://php.net/manual/en/function.gmp-mul.php](http://php.net/manual/en/function.gmp-mul.php)
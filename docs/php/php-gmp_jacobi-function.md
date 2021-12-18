# PHP|gmp_Jacobi()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_jacobi-function/](https://www.geeksforgeeks.org/php-gmp_jacobi-function/)

Gmp_Jacobi()函数是 PHP 中的一个内置函数，它计算作为参数传递给函数的两个 GMP 数字[(GNU 多精度：对于大数)](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)**$num1**和**$num2**的[Jacobi 符号](https://en.wikipedia.org/wiki/Jacobi_symbol)并返回。 **$num2**必须是正数和奇数。

**语法：**

```php
gmp_jacobi($num1, $num2)
```

**使用的参数：**
该函数接受两个必选参数**$num1**和**$num2**，如上面的语法所示。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以将数字字符串传递给函数，前提是可以将这些字符串转换为数字。

**返回值：**
此函数返回 GMP 编号(在 PHP 5.5 和更早版本中)或 GMP 对象(在 PHP 5.6 和更高版本中)，它是数字的 Jacobi。

**示例：**

```php
Input : $num1 = 2, $num2 = 3
Output : -1

Input : $num1 = 6, $num2 = 15
Output : 0

```

以下程序将演示 gmp_Jacobi()函数：

**程序 1**

```php
<?php
// PHP program to calculate the
// jacobi of two GMP numbers
$num1 = 13;
$num2 = 9907;

// Display the result
echo gmp_jacobi($num1, $num2); 
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2**

```php
<?php
// PHP program to calculate the
// jacobi of two GMP numbers

// creating GMP numbers using gmp_init()
$num1 = gmp_init("124567812");
$num2 = gmp_init("271290907");

//Display the result
echo gmp_jacobi($num1, $num2); 
?>
```

发帖主题：Re：Колибри0.7.0

```php
-1
```

**引用：**[http://php.net/manual/en/function.gmp-jacobi.php](http://php.net/manual/en/function.gmp-jacobi.php)
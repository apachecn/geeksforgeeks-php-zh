# PHP|GMP_RANDOM_RANGE()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_random_range-function/](https://www.geeksforgeeks.org/php-gmp_random_range-function/)

**GMP_RANDOM_RANGE()**是 PHP 中的一个内置函数，它生成一个随机数，因此生成的随机数介于 min 到 max 之间。 这里的 GMP 指的是([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))，它代表大数。

**语法：**

```php
gmp_random_range ( GMP $min, GMP $max )
```

**参数：**函数接受两个参数，gmp*$min*number 表示随机数的下界，gmp*$max*number 表示随机数的上界。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回$min-$max 范围内的随机 GMP 编号。

例如：

```php
Input : lower bound=0, upper bound =100
Output :  25

Input : lower bound=-100, upper bound=-10
Output :  -23 

Note:Output will vary every time on execution

```

以下程序说明了**GMP_RANDOM_RANGE()**函数的用法：

**程序 1：**下面的程序演示了将数字字符串作为参数传递时 gmp_Random_range()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_random_range() function 

// numeric string as arguments
$min = "-200";
$max = "-100";

$rand = gmp_random_range($min, $max); 

echo $rand;
?>
```

产出：

```php
-165
```

**程序 2：**下面的程序演示了将 GMP 编号作为参数传递时 GMP_RANDOM_RANGE()的工作方式。

```php
<?php
// PHP program to demonstrate the gmp_random_range() function 

// GMP numbers as arguments
$min = gmp_init("1000", 2);
$max = gmp_init("1000000", 2); 

$rand = gmp_random_range($min, $max); 

// gmp_strval converts GMP number to string 
// representation in given base(default 10).
echo gmp_strval($rand) . "\n";
?>
```

产出：

```php
30
```

**引用：**
[http://php.net/manual/en/function.gmp-random-range.php](http://php.net/manual/en/function.gmp-random-range.php)
# PHP|GMP_SCAN1()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_scan1-function/](https://www.geeksforgeeks.org/php-gmp_scan1-function/)

GMP_SCAN1()是一个内置函数，用于从给定索引开始扫描 GMP 编号中的“1”([GNU Multiple Precision：for Large Number](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))，该索引向数字中的最高有效位移动。

**语法：**

```php
gmp_scan1($num, $index)
```

**参数：**此函数接受两个参数，如下所述：

*   **$num**：该参数为 GMP 号，必须传递。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
*   **$index**：此参数表示我们希望从其开始搜索的数字$num 的按位表示形式中的索引或位置。

**返回值：**此函数返回数字中找到“1”的位置。

例如：

```php
Input : gmp_scan1("101111101", 6)
Output : 8

Input : gmp_scan1("111001111", 2)
Output : 3

```

以下程序说明了 PHP 中的 gmp_scan1()函数：

**程序 1：**当作为 GMP 编号的数字串作为参数传递时，查找 GMP 编号中“1”位的位置的程序。

```php
<?php

// PHP program to find position of "1" bit in GMP
// number passed as arguments

// strings as GMP numbers
$num = "10110001";
$pos = 2;

echo gmp_scan1($num, $pos) . "\n";

?>
```

产出：

```php
4

```

**程序 2：**当 GMP 编号作为参数传递时，查找 GMP 编号中“1”位的位置的程序。

```php
<?php
// PHP program to find position of "1" bit in GMP
// number

//creating GMP numbers using gmp_init()
$num = gmp_init(10001111101);
$pos = 2;

echo gmp_scan1($num, $pos) . "\n";

?>
```

产出：

```php
3

```

**引用：**
[http://php.net/manual/en/function.gmp-scan1.php](http://php.net/manual/en/function.gmp-scan1.php)
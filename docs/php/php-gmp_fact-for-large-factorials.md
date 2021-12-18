# PHP|大阶乘的 GMP_FACT()

> Original: [https://www.geeksforgeeks.org/php-gmp_fact-for-large-factorials/](https://www.geeksforgeeks.org/php-gmp_fact-for-large-factorials/)

GMP_FACT()是 PHP 中的一个内置函数，用于计算 GMP 数的阶乘([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```
gmp_fact ( $num )
```

**参数：**此函数接受 GMP 编号作为必选参数，如上面的语法所示。 它可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以是一个数字字符串，前提是可以将后者转换为数字。此函数计算该数字的阶乘并返回它。

**返回值：**此函数返回一个 GMP 数，它是作为参数传递的数的阶乘。

例如：

```
Input : "9"
Output : 362880

Input : 25
Output : 15511210043330985984000000

```

下面的程序演示了 PHP 中的 gmp_act()函数：

**程序 1：**

```
<?php
$fact = gmp_fact(5); 
echo gmp_strval($fact);

?>
```

产出：

```
120

```

**程序 2：**

```
<?php
$fact = gmp_fact(25); 
echo gmp_strval($fact);

?>
```

产出：

```
15511210043330985984000000

```

**引用：**
[http://php.net/manual/en/function.gmp-fact.php](http://php.net/manual/en/function.gmp-fact.php)
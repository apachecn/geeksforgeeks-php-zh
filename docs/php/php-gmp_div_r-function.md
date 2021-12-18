# PHP|gmp_div_r()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_div_r-function/](https://www.geeksforgeeks.org/php-gmp_div_r-function/)

gmp_div_r()函数是 PHP 中的一个内置函数，它执行两个 GMP 数字[(GNU 多精度：对于大数)](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)之间的除法运算，并返回余数。
**语法：**

```
gmp_div_r($num1, $num2)
```

**参数：**此函数接受两个 GMP 编号$num1 和$num2 作为必选参数，如上面的语法所示。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以将数字字符串传递给函数，前提是可以将这些字符串转换为数字。

**返回值：**此函数返回一个 GMP 编号，它是除法的余数。

**示例：**

```
Input : $num1 = 146, $num2  = 12
Output : 2

Input : $num1 = "189126457831", $num2  = "12098123409"
Output :  7654606696

```

下面的程序将说明 gmp_div_r()函数的用法。

**程序 1：**当 GMP 编号作为参数传递时执行 GMP 编号除法的程序。

```
<?php
// PHP program to perform the division of
// GMP numbers

// creating GMP numbers using gmp_init()
$num1 = gmp_init(257);
$num2 = gmp_init(17);

// caluates the remainder when 
//  $num1 is divided by num2

$res = gmp_div_r($num1, $num2);
// Display the remainder
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
2
```

**程序 2：**当作为 GMP 编号的数字字符串作为参数传递时，执行 GMP 编号除法的程序。

```
<?php
// PHP program to perform the division of
// GMP numbers

// creating GMP number using gmp_init()
$a = gmp_init("7891267541121");

// calculates the remainder when 
// $a is divided by 115789034
$res = gmp_div_r($a, 115789034);

// Display the remainder
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
13295953
```

**参考：**http://php.net/manual/en/function.gmp-div-r.php
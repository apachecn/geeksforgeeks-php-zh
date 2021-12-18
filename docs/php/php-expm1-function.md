# PHP|expm1()函数

> Original: [https://www.geeksforgeeks.org/php-expm1-function/](https://www.geeksforgeeks.org/php-expm1-function/)

欧拉数或俗称**e**是一个非常流行的无理数，它近似于 2.718281828，是最重要的数学常数之一。 E 是自然对数系统的底数。 指数值被广泛应用于许多场合，如复利、伯努利试验、正态分布、微积分等。

**expm1()**函数是 PHP 中的内置函数，用于计算 e 的给定参数的幂减一。

**语法：**

```php
*float* expm1($power)
```

**参数：**此函数接受单个参数**$power**，该参数定义 e 必须提升到的幂。

**返回值：**此函数返回一个浮点值，该值是 e 的值乘以给定参数-1 的**$幂**。 也就是说，它将返回(e<sup>$power</sup>-1)。

例如：

```php
Input : $power = 1 
Output : (e1-1) = 1.718281828459

Input : $power = 0 
Output : (e0-1) = 0 

```

下面的程序演示了 PHP 中的 expm1()函数：

**程序 1：**演示 expm1()函数的 PHP 程序。

```php
<?php
// PHP program to demonstrate the expm1() function 

$n1 = 1; 
$n2 = 0; 

//prints value of e^1 - 1 
echo "e^", $n1, "-1 = ", expm1($n1), "\n"; 

//prints value of e^0 - 1 
echo "e^", $n2, "-1 = ", expm1($n2), "\n"; 

?>
```

产出：

```php
e^1-1 = 1.718281828459
e^0-1 = 0

```

**程序 2：**使用数组演示 expm1()函数的 PHP 程序。

```php
<?php

// PHP code to illustrate the working 
// of expm1() Function 

// input array 
$array = array(2, 3, 1, 5); 

// print all the e^x-1 value in the arrays
foreach($array as $i)
    echo 'e^'.$i.'-1 = '.expm1($i)."\n";

?>
```

产出：

```php
e^2-1 = 6.3890560989307
e^3-1 = 19.085536923188
e^1-1 = 1.718281828459
e^5-1 = 147.41315910258

```

**参考**：
[http://php.net/manual/en/function.expm1.php](http://php.net/manual/en/function.expm1.php)
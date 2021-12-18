# 比较 PHP 中的浮点值

> 原文:[https://www.geeksforgeeks.org/comparing-float-value-in-php/](https://www.geeksforgeeks.org/comparing-float-value-in-php/)

在 PHP 中，浮点值的大小取决于平台。由于浮点数的内部表示，在执行或测试浮点值是否相等时，可能会出现意外的输出。例如，请参见以下程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare valuable and initialize it
$value1 = 8 - 6.4;
$value2 = 1.6;

// Compare the values
if($value1 == $value2) {
    echo 'True';
}
else {
    echo 'False';
}

?>
```

**Output:** 

```
False
```

**解释:**这段代码的输出是 false，这是非常不可预测的，但是在 PHP 中，值 1 并不完全是 1.6，也就是说，它来自 8 和 6.4 之间的差异，实际上是 1.599999，这就是为什么这个语句被证明是 False。

**如何解决上述问题？**
**方法 1 :** 对于浮点值的相等性测试，使用机器ε或者我们可以称之为计算机系统中计算的最小差异。

**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to compare floating values

// Declare variable and initializing
// it by floating value
$value1 = 1.23456789;
$value2 = 1.23456780;
$epsilon = 0.00001;

// Use absolute difference and compare values
if(abs($value1 - $value2) < $epsilon) {
    echo "True";
}
else {
    echo "False";
}

?>
```

**Output:** 

```
True
```

**说明:**在本代码中，使用两个浮点数*值 1* 和*值 2* 以及*ε*。现在，通过使用名为 *abs()* 的预定义函数，获取值的绝对差值(值 1 和值 2)。这段代码将给出绝对值，但问题是为什么我们要取绝对值。您可以看到这两个值在小数点后都有相同的数字，直到精度值 7。这对于系统来说很难分析比较。

**方法二:**我们可以在 PHP 中使用[舍入函数。](https://www.geeksforgeeks.org/php-round-function/)

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to compare floating values

// Declare valuable and initialize it
$value1 = 8 - 6.4;
$value2 = 1.6;

// Use round function to round off the
// floating value upto two decimal place
// and then compare it.
var_dump(round($value1, 2) == round($value2, 2));

?>
```

**Output:** 

```
bool(true)
```
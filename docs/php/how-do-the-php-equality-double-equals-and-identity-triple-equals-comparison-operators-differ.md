# PHP 等式(== double equals)和等式(=== triple equals)比较运算符有何不同？

> 原文:[https://www . geesforgeks . org/how-the-PHP-equality-double-equals-and-identity-triple-equals-comparison-operators-different/](https://www.geeksforgeeks.org/how-do-the-php-equality-double-equals-and-identity-triple-equals-comparison-operators-differ/)

**相等运算符==**

称为等号运算符的比较运算符是双等号“==”。该运算符接受两个输入进行比较，如果两个值都相同，则返回真值(它只比较变量值，不比较数据类型)，如果两个值不相同，则返回假值。

这一点应该始终牢记，目前的等式运算符==不同于赋值运算符=。赋值运算符改变并赋值左边的变量，使其有一个新值作为右边的变量，而**等号运算符==测试等式**，并根据比较结果返回真或假。

**例:**

```
<?php

// Variable contains integer value
$x = 999;

// Vatiable contains string value
$y = '999';

// Compare $x and $y
if ($x == $y)
    echo 'Same content';
else
    echo 'Different content';
?>
```

**输出:**

```
Same content

```
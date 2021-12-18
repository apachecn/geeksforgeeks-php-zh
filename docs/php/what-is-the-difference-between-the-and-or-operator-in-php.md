# PHP 中的|和|| or 运算符有什么区别？

> 原文:[https://www . geeksforgeeks . org/什么是 php 中的 and or 运算符/](https://www.geeksforgeeks.org/what-is-the-difference-between-the-and-or-operator-in-php/)

**'| '操作员**

它是按位*或*运算符。如果设置了 a 或 b 或两者，该运算符用于设置操作数的位。这意味着该位的值将设置为 1。T20【0】T24】1T27T32】1T36】1

| A | B | 甲&#124;乙 |
| --- | --- | --- |
| Zero | Zero | Zero |
| one |
| one | Zero |

**语法:**

```
$a | $b
```

**程序:**

```
<?php
$a = 3;
$b = 10;
echo $a | $b;
?>
```

**输出:**

```
11

```
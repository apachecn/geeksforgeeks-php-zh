# PHP 中$GLOBALS 有什么用？

> 原文:[https://www . geesforgeks . org/PHP 中的 globals 有什么用处/](https://www.geeksforgeeks.org/what-is-the-use-of-globals-in-php/)

在本文中，我们将讨论 PHP 中的 [$GLOBALS](https://www.geeksforgeeks.org/how-to-declare-a-global-variable-in-php/) 。$GLOBALS 是一个[超全局](https://www.geeksforgeeks.org/php-superglobals/)变量，用于从 PHP 程序的任何地方访问全局变量。PHP 将所有全局变量存储在一个名为$GLOBALS[index]的数组中。

**语法:**

```php
$GLOBALS['index']=value;
```

*   值是输入值。
*   索引是特定值的唯一键。

**示例:** PHP 程序演示$GLOBALS。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 

// Initialize an index A
// and set to 100
$GLOBALS['A'] = 100;

// Display
echo $A;
echo "<br>";

// Initialize an index A
// and set to a string
$GLOBALS['B'] = "This is Global";

echo "\n";
echo $B;

?>
```

**输出:**

```php
100
This is Global
```

**示例 2:** 使用$GLOBALS 执行算术运算的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 

// Initialize an A index and set to 100
$GLOBALS['A'] = 100;

// Initialize an B index and set to 200
$GLOBALS['B'] = 200;

// Display addition
echo $GLOBALS['A']+$GLOBALS['B'];
echo "<br>";

// Display subtraction
echo $GLOBALS['A']-$GLOBALS['B'];
echo "<br>";

// Display multiplication
echo $GLOBALS['A']*$GLOBALS['B'];
echo "<br>";

// Display division
echo $GLOBALS['B']/$GLOBALS['A'];
echo "\n";

?>
```

**输出:**

```php
 300
-100
 20000
 2
```
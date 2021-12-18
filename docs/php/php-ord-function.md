# PHP|order()函数

> Original: [https://www.geeksforgeeks.org/php-ord-function/](https://www.geeksforgeeks.org/php-ord-function/)

**order()**函数是 PHP 中的一个内置函数，它返回字符串第一个字符的 ASCII 值。 此函数接受字符串作为参数，并返回该字符串第一个字符的 ASCII 值。

**语法：**

```
*int* ord($string)
```

**参数：**此函数接受单个参数*$string*。 这是一个强制参数，我们可以从中获取 ASCII 值。

**返回值：**此函数返回一个整数值，表示作为参数传递给此函数的字符串中第一个字符的 ASCII 值。

**示例：**

```
Input : Geeksforgeeks
Output : 71
Explanation: The ASCII value of G is 71

Input : twinkle
Output : 116
Explanation: The ASCII value of t is 116

```

下面的程序演示了 PHP 中的 order()函数：

**程序 1：**

```
<?php
// PHP program to illustrate the ord() function

// ASCII value of 't' is printed.
echo ord("twinkle");
?>
```

产出：

```
116

```

**程序 2：**

```
<?php
// PHP program to illustrate the ord() function

// ASCII value of 'G' is printed
echo ord("Geeksforgeeks");
?>
```

产出：

```
71
```

**引用：**
[http://php.net/manual/en/function.ord.php](http://php.net/manual/en/function.ord.php)
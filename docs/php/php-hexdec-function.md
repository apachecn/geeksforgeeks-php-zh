# PHP|hedec()函数

> Original: [https://www.geeksforgeeks.org/php-hexdec-function/](https://www.geeksforgeeks.org/php-hexdec-function/)

十六进制是以 16 为基数的位置数字系统。它有 16 个不同的符号，其中前 9 个符号是 0-9，表示 0 到 9 的值，其余 6 个符号是 A，B，C，D，E，F，分别表示 10 到 15 的值。 由于十六进制数字代表四个二进制数字，因此它允许以更友好的方式表示二进制编码值，因此它比其他数字系统(如二进制和八进制)更受欢迎。

PHP 中的*hedec()*函数将十六进制数转换为十进制数。
函数的作用是：转换太大而不适合整数类型的数字，在这种情况下，较大的值将作为浮点数返回。 如果十六进制解码器()遇到任何非十六进制字符，它会忽略它们。

**语法：**

```php
hexdec($value)
```

**参数：**hedec()函数接受单个参数*$value*。 它是要计算其十进制等价物的十六进制数。

**返回值：**PHP 中的 hexdec()函数返回相当于十六进制数的十进制。

例如：

```php
Input : hexdec("5e")
Output : 94

Input : hexdec("a")
Output : 10

Input : hexdec("f1f1")
Output : 61937

Input : hexdec("abc451")
Output : 11256913

```

下面的程序演示了十六进制解码器()在 PHP 中的工作原理：

```php
<?php

echo hexdec("5e") . "\n";
echo hexdec("a") . "\n";
echo hexdec("f1f1") . "\n";
echo hexdec("abc451") . "\n";

?>
```

产出：

```php
94
10
61937
11256913

```

**需要注意的重要事项：**

*   它将十六进制数转换为等价的十进制数。
*   如果数字太大而不能作为整数类型返回，则它以浮点数的形式返回值。
*   十六进制数字系统是当今最流行和使用最广泛的数字系统之一。

**参考**：
[http://php.net/manual/en/function.hexdec.php](http://php.net/manual/en/function.hexdec.php)
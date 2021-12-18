# PHP|煎熬()函数

> Original: [https://www.geeksforgeeks.org/php-decoct-function/](https://www.geeksforgeeks.org/php-decoct-function/)

在计算的早期，八进制数和八进制计数系统非常流行来计算输入和输出，因为当它以 8 为单位工作时，输入和输出是以 8 为单位计数的，一次一个字节。 由于八进制数系统的广泛使用，我们经常需要将十进制数转换成它的十进制八进制表示法。有很多方法可以将十进制数转换成它的八进制数，但是它们有点耗时。但是 PHP 提供了一个内置的函数，可以用来将十进制数转换成它的八进制数。

PHP 中的 Formpt()函数用于返回相当于十进制数的八进制数。
对于 32 位平台，可以转换的最大数字通常是十进制数 4294967295，结果是 37777777777，而在 64 位平台中，十进制数通常是 9223372036854775807，结果是 77777777777777777。

**语法：**

```php
*string* decoct(value)
```

**参数：**此函数接受单个参数*值*。 它是要计算其八进制等值的十进制数。

**返回值：**PHP 中的 Formpt()函数返回一个字符串，该字符串表示作为参数传递给它的十进制数的八进制值。

例如：

```php
Input : decoct("35")
Output : 45

Input : decoct("67")
Output : 103

Input : decoct("4294967295")
Output : 37777777777

```

下面的程序演示了 PHP 中 Unifft()的工作原理：

```php
<?php

echo decoct("35") . "\n";
echo decoct("67") . "\n";
echo decoct("4294967295") . "\n";

?>
```

产出：

```php
43
103
37777777777

```

**需要注意的重要事项：**

*   它将十进制数转换为等价的八进制数。
*   此函数支持负数。
*   现在八进制数系统不像十六进制数系统那样流行。

**参考**：
[http://php.net/manual/en/function.decoct.php](http://php.net/manual/en/function.decoct.php)
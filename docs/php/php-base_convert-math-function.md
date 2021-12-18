# PHP | base_convert()数学函数

> 原文:[https://www . geesforgeks . org/PHP-base _ convert-math-function/](https://www.geeksforgeeks.org/php-base_convert-math-function/)

PHP 中的 *base_convert()* 函数用于将任意基数给定的数字转换为所需的基数。
碱基应该在 2 到 32 之间，数字大于 10 的碱基用字母 a-z 表示，即 10 表示为 a，11 表示为 b，35 表示为 z。
字母的大小写不敏感。

**语法:**

```php
*string* base_convert($inpNumber, $fromBase, $desBase)

```

**使用的参数:**该功能接受三个参数，描述如下:

1.  $ inpNumber:这是要转换的数字。
2.  $fromBase:它是数字的原始基数。
3.  $desBase:它是您要转换为的基数。

**返回值:**返回一个字符串，代表转换为所需基数的数字。

**示例:**

```php
Input : base_convert(B296, 16, 8)
Output : 131226

Input : base_convert(B296, 16, 2)
Output : 1011001010010110

Input : base_convert(621, 8, 16)
Output : 191

Input : base_convert(110011, 2, 16)
Output : 33

```

下面的程序说明了 PHP 中的 base_convert()函数:

*   将十六进制转换为八进制:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$hexadec = "B296";
echo base_convert($hexadec, 16, 8);

?>     
```

**输出:**

```php
131226

```

*   将十六进制转换为二进制:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$hexadec = "B296";
echo base_convert($hexadec, 16, 2);

?>     
```

**输出:**

```php
1011001010010110

```

*   将八进制转换为十六进制:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$octal = "621";
echo base_convert($octal, 8, 16);

?>  
```

**输出:**

```php
191

```

*   将二进制转换为十六进制:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$binary = "110011";
echo base_convert($binary, 2, 16);

?>

```

**输出:**

```php
33

```

**参考**:
T3】http://php.net/manual/en/function.base-convert.phpT5】
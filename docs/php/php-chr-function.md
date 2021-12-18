# PHP | chr()函数

> 原文:[https://www.geeksforgeeks.org/php-chr-function/](https://www.geeksforgeeks.org/php-chr-function/)

**chr()** 函数是 PHP 中的内置函数，用于将 ASCII 值转换为字符。它接受一个 ASCII 值作为参数，并从指定的 ASCII 值中返回一个代表字符的字符串。ASCII 值可以用十进制、八进制或十六进制值指定。

*   八进制值由前导 0 定义。
*   十六进制值由前导 0x 定义。

**ASCII** 值表可以参考这里的[。](https://www.eecis.udel.edu/~amer/CISC651/ASCII-Conversion-Chart.pdf)

**语法**:

```php
*string* chr( $asciiVal)
```

**参数**:该函数接受单个参数*$ as lifal*。此参数包含有效的 ASCII 值。函数的作用是:返回我们传递给它的 ASCII 值的对应字符，作为参数$ asciiVal。

**返回值:**函数返回我们传递 ASCII 值的字符。

示例:

```php
Input :  ASCII=35 ASCII=043 ASCII=0x23
Output : # # # 
Explanation: The decimal, octal and hex value of '#' is 
35, 043 and 0x23 respectively

Input : ASCII=48 
Output : 0 

```

下面的程序说明了 PHP 中的 chr()函数:

**程序 1:** 当传递不同的 ASCII 码但它们的等价字符相同时，演示 chr()函数的程序。

```php
<?php
// PHP program to demonstrate the chr() function

$n1 = 35;
$n2 = 043;
$n3 = 0x23;

echo "The equivalent character for ASCII 35 in decimal is ";
echo chr($n1), "\n";// Decimal value

echo "The equivalent character for ASCII 043 in octal is ";
echo chr($n2), "\n"; // Octal value

echo "The equivalent character for ASCII 0x23 in hex is ";
echo chr($n3); // Hex value

?>
```

输出:

```php
The equivalent character for ASCII 35 in decimal is #
The equivalent character for ASCII 043 in octal is #
The equivalent character for ASCII 0x23 in hex is #

```

**程序 2:** 用数组演示 chr()函数的程序。

```php
<?php
// PHP program to demonstrate the chr() function
// in array 

$a=[48, 49, 50]; 
foreach($a as $i)
{
    echo "The character equivalent of 
                 ASCII value of ", $i, " is ";
    echo chr($i), "\n";
}

?>
```

输出:

```php
The character equivalent of ASCII value of 48 is 0
The character equivalent of ASCII value of 49 is 1
The character equivalent of ASCII value of 50 is 2

```
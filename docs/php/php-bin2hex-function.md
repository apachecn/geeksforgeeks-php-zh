# PHP | bin2hex()函数

> 原文:[https://www.geeksforgeeks.org/php-bin2hex-function/](https://www.geeksforgeeks.org/php-bin2hex-function/)

PHP 中的 **bin2hex()** 函数将字符串转换为十六进制值。转换是先用高位半字节按字节进行的。

**注意:**不是用来把表示二进制数字的字符串转换成十六进制的。

**语法:**

```php
bin2hex($string)
```

**参数:**该函数接受单个参数 *$string* 。这是将被转换为十六进制值的字符串。

**返回值:**函数返回参数中传递的字符串的十六进制值。

示例:

```php
Input : string = "geeks"
Output : 6765656b73

Input : string = "1111"
Output : 31313131 
Explanation: "1111" is converted to its hexadecimal 
values, it is not treated as a binary string, else the 
answer would have been F which is not in this case.

```

下面的程序说明了 PHP 中的 bin2hex()函数:

**程序 1:**

```php
<?php
// PHP program to demonstrate
// the bin2hex() function 

$str = "geeks";

echo bin2hex($str);

?>
```

输出:

```php
6765656b73

```

**程序 2:**

```php
<?php
// PHP program to demonstrate 
// the bin2hex() function 

$str = "1111";

echo bin2hex($str);

?>
```

输出:

```php
31313131 

```

**参考**:
T3】http://php.net/manual/en/function.bin2hex.php
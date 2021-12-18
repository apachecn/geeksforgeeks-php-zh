# PHP|gmp_clrbit()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_clrbit-function/](https://www.geeksforgeeks.org/php-gmp_clrbit-function/)

Gmp_clrbit()函数是 PHP 中的一个内置函数，它清除一点 GMP 编号[(GNU Multiple Precision)](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)。 函数的作用是：将 GMP 编号中指定**索引**处的位设置为**0**。 索引从最低有效位开始从零开始。

**语法：**

```php
gmp_clrbit( $num, $index )
```

**参数：**该函数接受两个必选参数**$num**和**$index**，如上面的语法所示。 这些参数是：-

*   **$num:** it can be a GMP numbering resource in PHP 5.5, a GMP object in PHP 5.6 and later, or you can pass numeric strings to a function, provided you can convert those strings to digits.
*   **$index:** Index of bits to clear. The index starts at 0, where index 0 represents the least significant bit.

**返回值：**此函数返回 GMP 编号(在 PHP 5.5 和更早版本中)或 GMP 对象(在 PHP 5.6 和更高版本中)，它是指定索引处的位设置为 0 后形成的数字。

**示例：**

```php
Input : $num = 255, $index = 0
Output : 254

Input : $num = 128, $index = 7
Output : 0

```

以下程序说明了 gmp_clrbit()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate
// gmp_clrbit() function
$num = gmp_init(255);

gmp_clrbit($num, 0); // index starts at 0, least significant bit

echo gmp_strval($num);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2**：

```php
<?php
// PHP program to illustrate
// gmp_clrbit() function
$num = gmp_init("314567128");

gmp_clrbit($num, 8); // index starts at 0, least significant bit

echo gmp_strval($num);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.gmp-clrbit.php](http://php.net/manual/en/function.gmp-clrbit.php)
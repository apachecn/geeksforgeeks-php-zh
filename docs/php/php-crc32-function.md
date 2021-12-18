# PHP|crc32()函数

> Original: [https://www.geeksforgeeks.org/php-crc32-function/](https://www.geeksforgeeks.org/php-crc32-function/)

Crc32()函数帮助我们计算字符串的 32 位[CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)或[循环冗余校验和多项式](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)。 此函数使用[CRC32 算法](https://en.wikipedia.org/wiki/Cyclic_redundancy_check#CRC-32_algorithm)。此函数可用于验证数据完整性。
然而，为了确保我们从 crc32()函数获得正确的字符串表示，我们需要使用 printf()或 print intf()函数的%u 格式化程序。 如果未使用%u 格式化程序，结果可能会显示不正确的负数。

**语法**：

```php
crc32($string)

```

**参数**：

*   **$string**：该参数指定要为其找到 crc32 多项式的字符串。

**返回值**：crc32()函数以整数形式返回给定字符串的 crc32 校验和。

例如：

```php
Input : Hello world.
Output : 2335835140

Input : Geeks For Geeks.
Output : 2551101144

```

下面的程序说明了 crc32()函数。

**程序 1：**此程序帮助我们计算字符串“Hello World”的 32 位 CRC，包括带%u 和不带%u。

```php
<?php
// PHP program illustrate the 
// crc32() function

$str1 = crc32("Hello world.");

// print without %u
echo 'Without %u: '.$str1."\n";

// print with %u
echo 'With %u: ';

printf("%u\n", $str1);
?>
```

产出：

```php
Without %u: 2335835140
With %u: 2335835140

```

**程序 2：**此程序帮助我们计算字符串“GeeksforGeeks.”的 32 位 CRC，包括带%u 和不带%u。

```php
<?php
$str2 = crc32("GeeksforGeeks.");

// print without %u
echo 'Without %u: '.$str2."\n";

// print with %u
echo 'With %u: ';

printf("%u\n", $str2);
?>
```

产出：

```php
Without %u: 3055367324
With %u: 3055367324

```

**程序 3：**此程序帮助我们计算字符串“Computer Science.”的 32 位 CRC，包括带%u 和不带%u。

```php
<?php
$str3 = crc32("Computer Science.");

// print without %u
echo 'Without %u: '.$str3."\n";

// print with %u
echo 'With %u: ';

printf("%u\n", $str3);
?>
```

产出：

```php
Without %u: 3212073516
With %u: 3212073516

```

**参考**：
[http://php.net/manual/en/function.crc32.php](http://php.net/manual/en/function.crc32.php)
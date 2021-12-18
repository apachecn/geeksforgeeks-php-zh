# PHP|strncasecmp()函数

> Original: [https://www.geeksforgeeks.org/php-strncasecmp-function/](https://www.geeksforgeeks.org/php-strncasecmp-function/)

strncasecmp()函数是 PHP 中的内置函数，用于比较两个给定的字符串。 它不区分大小写。 此函数类似于 strcasecmp()，唯一的区别是指定每个字符串中用于比较的字符数。

**语法：**

```php
strncasecmp($string1, $string2, $length)
```

**参数：**此函数接受上述语法中所示的两个参数，如下所示：

*   **$STRIN1，$STRIN2：**这些参数指定要比较的字符串。
*   **$length：**它指定要在比较中使用的每个字符串中的字符数。 此参数是必需的

**返回值：**此函数根据以下条件返回一个整数：

*   Strncasecmp()返回 0-如果两个字符串相等。
*   Strncasecmp()返回<0-如果字符串 1 小于字符串 2
*   Strncasecmp()返回>0-如果字符串 1 大于字符串 2

例如：

```php
Input : string1 = "Hello", string2 = "hEllo", length = 6
Output : 0

Input : string1 = "Geeks", string2 = "Gfg", length = 3
Output : -1

Input : string1 = "Nerd", string2 = "Geeks", length = 4
Output : 7

```

下面的程序演示了 PHP 中的 strncasecmp()函数：

**程序 1**：当两个字符串相同时：

```php
<?php

$str1 = "Geeks for Geeks ";
$str2 = "Geeks for Geeks ";

// Both the strings are equal
$test=strncasecmp($str1, $str2, 16 ); 

echo "$test"; 

?>
```

发帖主题：Re：Kolibrios

```php
0
```

**程序 2**：当第一个字符串大于第二个字符串时：

```php
<?php

// Input strings
$str1 = "Geeks for Geeks ";
$str2 = "Geeks for ";

$test=strncasecmp($str1, $str2, 16 ); 

// In this case the second string is smaller
echo "$test"; 

?>
```

产出：

```php
6
```

**程序 3**：第一个字符串小于第二个字符串：

```php
<?php

// Input Strings
$str1 = "Geeks for ";
$str2 = "Geeks for Geeks ";

$test=strncasecmp($str1, $str2, 16 ); 

// In this case the first string is smaller
echo "$test"; 

?>
```

产出：

```php
-6
```

**程序 4**：此程序说明函数不区分大小写：

```php
<?php

// Input Strings
$str1 = "GEEKS FOR GEEKS ";
$str2 = "Geeks for Geeks ";

// Both the strings are equal
$test=strncasecmp($str1, $str2, 16 ); 

echo "$test"; 

?>
```

产出：

```php
0
```

**程序 5**：两个字符串长度相等，但包含不同的字符。 在这种情况下，显示两个字符的 ASCII 值之间的差异。 如果字符串 1 中的字符具有较大的 ASCII 值，则该函数返回正值；如果字符串 2 中的字符具有较大的 ASCII 值，则该函数返回负值。

```php
<?php

// Input Strings 
$str1 = "Good";
$str2 = "Goon";

$test1 = strncasecmp($str1, $str2, 4 ); 

// Second string has a character 
// with higher ASCII value
echo "$test1"; 

echo "\n";

$test2 = strncasecmp($str2, $str1, 4 ); 

// First string has a character 
// with higher ASCII value
echo "$test2"; 

?>
```

产出：

```php
-10
10

```

**参考**：
[http://php.net/manual/en/function.strncasecmp.php](http://php.net/manual/en/function.strncasecmp.php)
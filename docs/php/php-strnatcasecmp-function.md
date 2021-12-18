# PHP|strnatcasecmp()函数

> Original: [https://www.geeksforgeeks.org/php-strnatcasecmp-function/](https://www.geeksforgeeks.org/php-strnatcasecmp-function/)

Strnatcasecmp()函数是 PHP 中的一个内置函数，它使用“自然顺序”算法比较该字符串。 此函数接受两个字符串作为参数，并返回整数值(正、负或零)。 该函数类似于 strnatcmp()，唯一的区别是该函数不区分大小写。

**语法：**

```php
strnatcasecmp( $string1, $string2 )
```

**参数：**该函数接受两个必需的字符串参数，如上面的语法所示。 这些参数定义如下：

*   **$String1:** this parameter specifies the first string to compare.
*   **$String2:** this parameter specifies the second string to compare.

**返回值：**此函数基于以下条件返回正整数、负数或 0：

*   Returns **0** if two strings are equal; if two strings are equal
*   Returns a positive value of **(> 0)** .
*   If $STRIN1 is less than $STRING 2, a negative value of **(< 0)** is returned.

例如：

```php
Input : $string = "Geek", $string2 = "GEEK"
Output : 0

Input : $string = "Geeks", $string2 = "Geek"
Output : 1

```

以下程序说明了 strnatcasecmp()函数：

**程序 1：**此程序说明了 strnatcasecmp()函数的简单用法。

```php
<?php

echo strnatcasecmp("Geeks", "Geek");

?>
```

帖子主题：Re：Колибрипрограммированияпрограмма

**程序 2：**此程序说明 strnatcasecmp()函数不区分大小写。

```php
<?php

// Case-insensitive strnatcasecmp() function
echo strnatcasecmp("Geeks", "GEEKS");
echo "\n";

// Case-sensitive strnatcmp() function
echo strnatcmp("Geeks", "GEEKS");

?>
```

帖子主题：Re：Колибрипрограммированияпрограмма
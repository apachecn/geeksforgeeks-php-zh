# PHP|strcspn()函数

> Original: [https://www.geeksforgeeks.org/php-strcspn-function/](https://www.geeksforgeeks.org/php-strcspn-function/)

Strcspn()函数是 PHP 中的一个内置函数，它返回在找到要搜索的指定字符的任何部分之前字符串中存在的字符数。 此函数区分大小写。

**语法：**

```php
strcspn( $string, $charlist, $start, $length)

```

**参数：**此函数接受四个参数，如上面的语法所示。 前两个参数是必需的，必须提供，而其余两个参数是可选的。 所有这些参数如下所述：

*   **$string：**此必选参数指定要搜索的字符串
*   **$charlist：**此强制参数指定要在给定$字符串中搜索的字符列表。
*   **$start：**此可选参数指定在字符串中开始搜索的索引。
    *   如果给定了$start 并且是**非负**，那么 strcspn()将从该位置开始检查$string。
    *   如果给定了$start 并且**为负**，则 strcspn()将从$string 的末尾开始从该位置开始检查$string。
*   **$length：**它指定需要搜索的$string 的字符数。 它的默认值是直到$字符串的末尾。
    *   如果给定$LENGTH 并且为**非负**，则将从起始位置检查$STRING 中的$LENGTH 字符。
    *   如果给定$LENGTH 并且为**负**，则将从$STRING 的起始位置直到$STRING 末尾的$LENGTH 字符检查$STRING。

**返回值：**返回在字符串中找到**$charlist**参数中的任何字符之前，字符串中从起始位置(包括空格)开始的字符数。

例如：

```php
Input : $string = "Geeks for Geeks", $charlist = "mnopqr"
Output : 7

Input : $string = "Geeks for Geeks", $charlist = "for"
Output : 6

```

下面的程序将说明 strcspn()函数的用法：

**程序 1：**此程序显示 strcspn()函数的简单用法。

## PHP

```php
<?php

// Output is 6 because the input string
// contains 6 characters "Geeks " before
// the first character 'f' from the list
// "for" is found in the string.
echo strcspn("Geeks for Geeks", "for");

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
6

```

**程序 2：**此程序显示 strcspn()函数区分大小写。

## PHP

```php
<?php

// Output is 7 because the input string
// does not contain 'F' as specified in the list "For".
// Hence the first character from the
// list that is present in the string is 'o'
echo strcspn("Geeks for Geeks", "For");

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
7

```

**程序 3：**此程序显示带有$start 参数的 strcspn()函数的用法。

## PHP

```php
<?php

// Searches from index 5 till
// the end of the string
echo strcspn("Geeks for Geeks", "G", 5);

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
5

```

**程序 4：**此程序说明了带负$length 参数的 strcspn()函数的用法。

## PHP

```php
<?php

// Searches from index 5 till 5-th position
// from end. Output is 0 since the character
// at $start (i.e. 5) is present in the
// specified list of characters
echo strcspn("Geeks for Geeks", " for", 5, -5);

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
0

```

**程序 5：**此程序显示带有负$start 参数的 strcspn()函数的用法。

## PHP

```php
<?php

// Searches from 5th index from the end of the string
// Output is 0 as the character 'G' in the
// specified starting index is present in the
// given list of characters to be checked.
echo strcspn("Geeks for Geeks", "Geek", -5);

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
0

```

**引用：**
[http://php.net/manual/en/function.strcspn.php](http://php.net/manual/en/function.strcspn.php)
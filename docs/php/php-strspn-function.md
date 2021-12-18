# PHP|strspn()函数

> Original: [https://www.geeksforgeeks.org/php-strspn-function/](https://www.geeksforgeeks.org/php-strspn-function/)

Strspn()函数是 PHP 中的一个内置函数，它查找字符串的起始段的长度，该字符串完全由作为参数传递给函数的给定字符列表中包含的字符组成。

**语法：**

```php
strspn( $string, $charlist, $start, $length)

```

**参数：**此函数接受四个参数，如上面的语法所示。 前两个参数是必需的，必须提供，而其余两个参数是可选的。 所有这些参数如下所述：

*   **$string：**此强制参数指定要搜索的字符串。
*   **$charlist：**此强制参数指定要在给定$字符串中搜索的字符列表。
*   **$start：**此可选参数指定要在字符串中开始搜索的索引。
    *   如果给定**$START**且非负，则 strspn()将从该位置开始检查**$STRING**。
    *   如果给定了**$start**并且为负值，则 strspn()将从$string 的末尾开始从该位置开始检查$string。
*   **$length：**它指定需要搜索的$string 的字符数。 它的默认值是直到$字符串的末尾。
    *   如果**$LENGTH**给定且非负，则将从起始位置检查$STRING 中的$LENGTH 字符。
    *   如果给定**$LENGTH**且为负数，则将检查从起始位置到$STRING 末尾的$LENGTH 字符的$STRING。

**返回值：**此函数返回在仅包含 charlist 参数中的字符的字符串中找到的字符数。

例如：

```php
Input : $string = "abcdefghijk", $charlist = "abcjkl"
Output : 3

Input : $string = "Geeks for Geeks", $charlist = "Geeksfor "
Output : 15

```

以下程序说明了 strspn()函数：

**程序 1：**

```php
<?php
// Output is 15 because whole input string
// contains all characters from given char list
// "Geeksfor "
echo strspn("Geeks for Geeks", "Geeksfor ");
?> 
```

发帖主题：Re：Колибри0.7.0

```php
15
```

**程序 2：**此程序说明 strspn()函数区分大小写。

```php
<?php
// Output is 0 because there is no substring
// which contains all characters of given char
// list.
echo strspn("Geeks for Geeks", "geeks");
?> 
```

发帖主题：Re：Колибри0.7.0

```php
0
```

**程序 3：**此程序说明如何使用带有$start 和$length 参数的 strspn()函数。

```php
<?php
// Searches substring starting from index 5 
// and length 9 with all characters in char 
// list " for"
echo strspn("Geeks for Geeks", " for", 5, 9);
?> 
```

发帖主题：Re：Колибри0.7.0

```php
5
```

**程序 4：**此程序说明了带负$length 参数的 strspn()函数的用法。

```php
<?php
// Searches from index 5 till 5-th position from
// end.
echo strspn("Geeks for Geeks", " for", 5, -5);
?> 
```

发帖主题：Re：Колибри0.7.0

```php
5
```

**程序 5：**此程序说明了带负$start 参数的 strspn()函数的用法。

```php
<?php
// Searches from 5-th index from end
echo strspn("Geeks for Geeks", "for", -5);
?> 
```

发帖主题：Re：Колибри0.7.0

```php
0
```

**引用：**
[http://php.net/manual/en/function.strspn.php](http://php.net/manual/en/function.strspn.php)
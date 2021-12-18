# PHP|strpbrk()函数

> Original: [https://www.geeksforgeeks.org/php-strpbrk-function/](https://www.geeksforgeeks.org/php-strpbrk-function/)

Strpbrk()函数是 PHP 中的一个内置函数，用于在字符串中搜索任何指定的字符。 此函数返回字符串的其余部分，从其中找到任何指定字符的第一个匹配项。 如果没有找到任何字符，则返回 False。 此函数是**区分大小写的**。

**语法：**

```php
strpbrk( $string, $charlist)
```

**参数：**此函数接受两个参数，如上面的语法所示。 这两个参数都是必需的，必须提供。 所有这些参数如下所述：

*   **$string：**此参数指定要搜索的字符串。
*   **$charlist：**此参数指定要查找的字符。

**返回值：**此函数返回从找到的字符开始的字符串，如果未找到，则返回 False。

例如：

```php
Input : $string = "Geeks for Geeks!", $charlist = "ef"
Output : eeks for Geeks!
Explanation : 'e' is the first occurrence of the specified 
characters. This function will, therefore, output "eeks for Geeks!", 
because it returns the rest of the string from where it found
the first occurrence of 'e'.

Input : $string = "A Computer Science portal", $charlist = "tue"
Output : uter Science portal

```

下面的程序将演示 PHP 中的 strpbrk()函数：

**程序 1：**

```php
<?php
echo strpbrk("Geeks for Geeks!", "ef"); 
?>
```

产出：

```php
eeks for Geeks!
```

**程序 2：**

```php
<?php
echo strpbrk("A Computer Science portal", "tue"); 
?>
```

产出：

```php
uter Science portal
```

**程序 3：**此程序将说明函数的区分大小写。

```php
<?php
echo strpbrk("A Computer Science portal", "c"); 
?>
```

产出：

```php
cience portal
```

**引用：**
[http://php.net/manual/en/function.strpbrk.php](http://php.net/manual/en/
function.strpbrk.php)
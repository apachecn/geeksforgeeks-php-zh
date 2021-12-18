# PHP|ltrim()函数

> Original: [https://www.geeksforgeeks.org/php-ltrim-function/](https://www.geeksforgeeks.org/php-ltrim-function/)

Ltrim()函数是 PHP 中的一个内置函数，用于从字符串左侧删除空格或其他字符(如果指定)。

**语法：**

```php
ltrim( $string, $charlist )
```

**参数：**函数 ltrim()接受两个参数，如上面的语法所示。 在这两个参数中，一个是强制的，另一个是可选的。 具体讨论如下：

*   **$string：**此强制参数指定要检查的字符串。
*   **$charlist：**此可选参数指定要从字符串中删除哪些字符。如果未提供此参数，将删除以下字符：
    *   **“\0”**-NULL
    *   “T0t”T1-制表符
    *   **“\n”**-新行
    *   **“\x0B”**-垂直制表符
    *   **“\r”**-回车
    *   **“”**-普通空格

**返回值：**返回修改后的字符串。

例如：

```php
Input : $string = "            Geeks for Geeks"
Output : Geeks for Geeks

Input : $string = "!!! (( !!)) Geeks for Geeks", $charlist = "! ()"
Output : Geeks for Geeks

```

以下程序说明了 ltrim()函数：

**程序 1：**此程序显示如何使用 ltrim()函数，而不使用任何指定的要删除的字符列表。

```php
<?php

$string = "            Geeks for Geeks";

echo "Contribute to ".ltrim($string);

?>
```

发帖主题：Re：Колибри0.7.0

```php
Contribute to Geeks for Geeks
```

**程序 2：**此程序显示如何使用 ltrim()函数以及指定的要删除的字符列表。

```php
<?php

$string = "!!! (( !!)) Geeks for Geeks";

// The characters '!', '(', ')', ' ' have 
// been specified to remove from the
// beginning of the string
echo ltrim($string, "! ()");

?>
```

发帖主题：Re：Колибри0.7.0

```php
Geeks for Geeks
```

**引用：**
[http://php.net/manual/en/function.ltrim.php](http://php.net/manual/en/function.ltrim.php)
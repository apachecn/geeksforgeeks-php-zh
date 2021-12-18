# PHP|strstr()函数

> Original: [https://www.geeksforgeeks.org/php-strstr-function/](https://www.geeksforgeeks.org/php-strstr-function/)

Strstr()函数是 PHP 中的内置函数。 它搜索一个字符串在另一个字符串中的第一个匹配项，并从前者在后者中的第一个匹配项开始显示后者的一部分(如果指定，则在此之前)。 此函数是**区分大小写的**。

**语法：↔**

```
strstr( $string, $search, $before )

```

**参数：**此函数接受上述语法中所示的三个参数，其中前两个参数必须提供，第三个参数是可选的。 所有这些参数如下所述：

*   **$string：**这是一个强制参数，指定要在其中执行搜索的字符串。
*   **$search：**它是指定要搜索的字符串的强制参数。 如果此参数是数字，它将搜索与数字的 ASCII 值匹配的字符
*   **$之前：**为可选参数。 它指定一个布尔值，其默认值为**False**。 如果设置为**true**，则返回$search 参数第一次出现之前的$string 部分。

**返回值：**此函数返回字符串的其余部分(从匹配点)，如果未找到要搜索的字符串，则返回 False。

例如：

```
Input : $string = "Hello world!", $search = "world"
Output : world!

Input : $string = "Geeks for Geeks!", $search = "k"
Output : ks for Geeks!

```

下面的程序演示了 PHP 中的 strstr()函数：

**程序 1：**在本程序中，我们将显示第一次出现$search 时的$string 部分。

## PHP

```
<?php
echo strstr("Geeks for Geeks!", "k");
?>
```

**输出：**

```
ks for Geeks! 

```

**程序 2：**在本程序中，我们将显示第一次出现$search 之前的$string 部分。

## PHP

```
<?php
echo strstr("Geeks for Geeks!", "k", true);
?>
```

**输出：**

```
Gee

```

**程序 3：**在此程序中，我们将传递一个整数作为$search。

## PHP

```
<?php
  $string = "Geeks";
  echo strstr($string, 101); // 101 is ASCII value of lowercase e
?>
```

**输出：**

```
eeks

```

**参考**：
[http://php.net/manual/en/function.strstr.php](http://php.net/manual/en/function.strstr.php)
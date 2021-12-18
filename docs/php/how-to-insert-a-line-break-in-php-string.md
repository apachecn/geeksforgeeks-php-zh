# 如何在 PHP 字符串中插入换行符？

> 原文:[https://www . geeksforgeeks . org/如何插入换行 php 字符串/](https://www.geeksforgeeks.org/how-to-insert-a-line-break-in-php-string/)

在本文中，我们将讨论如何在 PHP 字符串中插入换行符。我们将通过使用[**<u>nl2br()</u>**T5】功能来获得它。该函数用于在放置“\n”的地方添加新的换行符。](https://www.geeksforgeeks.org/php-nl2br-function/)

**语法:**

```
nl2br("string \n");
```

其中，字符串是输入字符串。

**示例 1:** 在字符串中插入换行符的 PHP 程序。

## PHP

```
<?php

// Insert a new line break
echo nl2br("This is first line \n This is second line");

?>
```

**输出**

```
This is first line <br />
 This is second line
```

**例 2:**

## PHP

```
<?php

// Insert a line break with new line
echo nl2br("This is first line \n This is second "
   + "line \n This is third line \n This is forth line");

?>
```

**输出**

```
This is first line <br />
 This is second line <br />
 This is third line <br />
 This is forth line
```
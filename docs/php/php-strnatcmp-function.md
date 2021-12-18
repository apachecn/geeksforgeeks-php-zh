# PHP|strnatcmp()函数

> Original: [https://www.geeksforgeeks.org/php-strnatcmp-function/](https://www.geeksforgeeks.org/php-strnatcmp-function/)

Strnatcmp()是 PHP 的内置函数。 此函数使用“自然顺序”算法比较两个字符串，并返回正整数、负整数或零。 此函数区分大小写。

**语法：**

```
strnatcmp( $string1, $string2 )
```

**参数：**函数接受两个必需的字符串参数进行比较，如上面的语法所示。

*   **$string 1：**此参数指定要比较的第一个字符串。
*   **$string 2：**此参数指定要比较的第一个字符串。

**返回值：**此函数根据以下条件返回整数值：

*   如果两个字符串相等，则函数返回**0**。
*   如果$STRIN1 小于$STRING 2，则函数返回**负值(<0)**。
*   如果$STRIN2 小于$STRIN1，则该函数返回**正值(>0)**。

例如：

```
Input : $string1 = "Hello", $string2 = "HEllo"
Output : 1

Input : $string1 = "Geek", $string2 = "Geeks"
Output : -1

```

以下程序说明了 PHP 中的 strnatcmp()函数：

**程序 1：**此程序显示 strnatcmp()函数的简单用法。

```
<?php

    echo strnatcmp("Geek", "Geeks");

?>
```

发帖主题：Re：Колибри0.7.8.0

```
-1
```

**程序 2：**此程序显示 strnatcmp()函数区分大小写。

```
<?php

    echo strnatcmp("Geeks", "GEEks");

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1
```

**程序 3：**此程序说明了 strcmp()和 strnatcmp()函数之间的区别。

```
<?php

    echo strnatcmp("Geek of month 2", "Geek of month 10");
    echo "\n";
    echo strcmp("Geek of month 2", "Geek of month 10");

?>
```

发帖主题：Re：Колибри0.7.8.0

```
-1
256
```

> **解释：**在自然算法中，数字 2 小于数字 10，而在计算机排序中，由于“10”中的第一个数字小于 2，10 被认为小于 2。

**引用：**
[http://php.net/manual/en/function.strnatcmp.php](http://php.net/manual/en/function.strnatcmp.php)
# PHP|substr_Compare()函数

> Original: [https://www.geeksforgeeks.org/php-substr_compare-function/](https://www.geeksforgeeks.org/php-substr_compare-function/)

*substr_Compare()*函数是 PHP 中的一个内置函数，它帮助比较从指定起始位置到指定长度的两个字符串。

**语法：**

```
*int* substr_compare($str1, $str2, $startpos, $len, $caseInsensitive)

```

**参数：**此函数总共接受五个参数，其中前三个参数为必填参数，其余两个参数为可选参数。 所有这些参数如下所述：

1.  **$str1**(必选)：此参数表示要比较的第一个字符串。
2.  **$str2**(必选)：此参数表示要比较的第二个字符串。
3.  **$startpos**(必需)：此参数指定在$str1 中开始比较的位置。 如果 startpos 为负，则从字符串末尾开始比较。
4.  **$len**(可选)：此参数指定要比较的$str1 的多少。
5.  **$caseInSensition**(可选)：该参数表示一个布尔值，用于指定是否执行区分大小写的比较。 如果设置为 False，则比较将区分大小写；如果设置为 True，则比较将不区分大小写

**返回值：**此函数根据以下情况返回整数值：

*   如果从位置$startpos 开始的$str1 小于 str2，则返回小于 0 的值。
*   如果$str1 从位置$startpos 开始大于字符串 2，则返回大于 0 的值。
*   如果$str1 和$str2 相等，则返回 0。
*   如果$startpos 等于或大于$str1 的长度，或者设置的长度$len 小于 1，则 substr_Compare()函数打印警告并返回 FALSE。

下面的程序演示了 PHP 中的 substr_Compare()函数：

```
<?php

// PHP program to illustrate the
// substr_compare() function

echo substr_compare("geeks", "gfg", 2)."\n";
echo substr_compare("geeksforgeeks", "gfg", 2)."\n";
echo substr_compare("Geeks", "gfg", 0, 1, true)."\n";
echo substr_compare("Geeks", "gfg", 0, 3, true)."\n";
echo substr_compare("GeeksforGeeks", "geeksforgeeks",
                                    0, false)."\n";

?>
```

产出：

```
-2
-2
0
-1
0

```

**参考**：
[http://php.net/manual/en/function.substr-compare.php](http://php.net/manual/en/function.substr-compare.php)
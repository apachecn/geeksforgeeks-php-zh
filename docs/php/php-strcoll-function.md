# PHP|strcoll()函数

> Original: [https://www.geeksforgeeks.org/php-strcoll-function/](https://www.geeksforgeeks.org/php-strcoll-function/)

**strcoll()**是 PHP 中的内置函数，用于比较两个字符串。 此函数区分大小写，指出在比较期间将区别对待大写和小写。 此函数用于比较两个字符串，并告诉我们第一个字符串是大于还是小于第二个字符串，还是等于第二个字符串。

**语法：**

```
strcoll($string1, $string2)
```

**参数：**该函数接受两个必需的字符串参数，如下所述。

1.  **$string 1：**此参数引用要在比较中使用的第一个字符串。
2.  **$string 2：**此参数引用要在比较中使用的第二个字符串。

**返回值**：该函数根据匹配条件返回一个随机整数值，其表达式为：

*   如果字符串相等，则返回 0。
*   如果$STRIN1 小于$STRING 2，则返回负值(<0)。
*   如果$STRIN2 小于$STRIN1，则返回正值(>0)。

**示例：**

```
Input : $string1 = "geeks for geeks" $string2="geeks for geeks"
Output : 0 

Input : $string1 = "striver" $string2="raj" 
Output : 1 

```

以下程序说明了 strcoll()函数的用法：

**程序 1：**下面的程序演示了传递两个相等字符串时的返回值

```
<?php
    //PHP program to compare two strings using 
    // strcoll() function (two strings are equal)
    $string1 = "geeks for geeks";
    $string2 = "geeks for geeks";

    // prints 0 as two strings are equal
    echo strcoll($string1, $string2);
?>
```

发帖主题：Re：Колибри0.7.0

```
0

```

**程序 2：**下面的程序演示字符串 1 大于字符串 2 时的返回值

```
<?php
    //PHP program to compare two strings using 
    // strcoll() function (string1>string2)
    $string1 = "striver";
    $string2 = "raj";

    // prints > 0 
    echo strcoll($string1, $string2);
?>
```

发帖主题：Re：Колибри0.7.0

```
1

```

**程序 3：**下面的程序演示字符串 2 大于字符串 1 时的返回值

```
<?php
    //PHP program to compare two strings using 
    // strcoll() function (string2>string1)
    $string1 = "CPP";
    $string2 = "PHP";

    // prints <0
    echo strcoll($string1, $string2);
?>
```

发帖主题：Re：Колибри0.7.0

```
-13

```

**参考**：
[http://php.net/manual/en/function.strcoll.php](http://php.net/manual/en/function.strcoll.php)
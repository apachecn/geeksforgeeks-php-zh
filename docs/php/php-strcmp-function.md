# PHP|strcmp()函数

> Original: [https://www.geeksforgeeks.org/php-strcmp-function/](https://www.geeksforgeeks.org/php-strcmp-function/)

比较两个字符串是编程和 Web 开发实践中最常用的字符串操作之一。 Strcmp()是 PHP 中的内置函数，用于比较两个字符串。 此函数区分大小写，指出在比较期间将区别对待大写和小写。 此函数用于比较两个字符串，并告诉我们第一个字符串是大于还是小于第二个字符串，还是等于第二个字符串。

**语法：**

```php
strcmp($string1, $string2)
```

**参数：**此函数接受两个参数，如下所述：

1.  **$string1**(必选)：该参数是指比较中使用的第一个字符串
2.  **$string2**(必选)：该参数指的是比较中使用的第二个字符串。

**返回值：**该函数根据匹配条件返回一个随机整数值，其表达式为：

*   如果字符串相等，则返回 0。
*   返回负值(<0), if *$STRIN2*大于*$STRIN1*。
*   如果*$STRING 1*大于*$STRING 2*，则返回正值(>0)。

在此代码中，我们将尝试了解 strcmp()函数的工作原理：

```php
<?php

// PHP program to illustrate the working of strcmp()
$string1 = "Welcome to GFG";
$string2 = "Welcome to GeeksforGeeks";
$string3 = "Welcome to GFG";

// In this case both the strings are equal
print_r(strcmp($string1, $string3));
echo "\n";

// In this case the first is greater
print_r(strcmp($string2, $string1));
echo "\n";

// In this case the second is greater
print_r(strcmp($string3, $string2))

?>
```

产出：

```php
0
31
-31
```

**参考**：
[http://php.net/manual/en/function.strcmp.php](http://php.net/manual/en/function.strcmp.php)
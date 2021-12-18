# PHP strlen()函数

> Original: [https://www.geeksforgeeks.org/php-strlen-function/](https://www.geeksforgeeks.org/php-strlen-function/)

在本文中，我们将了解如何使用 PHP 中的**strlen()**函数获取字符串的长度，并通过示例了解其实现。

**strlen()**是 PHP 中的一个内置函数，它返回给定字符串的长度。 它接受字符串作为参数，并返回其长度。 它计算字符串的长度，包括所有空格和特殊字符。

**语法：**

```php
strlen($string);
```

**参数：**strlen()函数只接受一个参数*$string*，这是必需的。 此参数表示需要返回其长度的字符串。

**返回值：**此函数返回*$字符串*的长度，包括所有空格和特殊字符。

下面的程序演示了 PHP 中的 strlen()函数：

**示例 1：**下面的示例演示了 PHP 中**strlen()**函数的使用。

## PHP

```php
<?php

    // PHP program to find the
    // length of a given string
    $str = "GeeksforGeeks";

    // prints the length of the string
    // including the space
    echo strlen($str);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**此示例演示了在字符串具有特殊字符和转义序列的情况下使用**strlen()**函数。

## PHP

```php
<?php

    // PHP program to find the
    // length of a given string which has
    // special characters
    $str = "\n GeeksforGeeks Learning;";

    // here '\n' has been counted as 1
    echo strlen($str);
?>
```

发帖主题：Re：Колибри0.7.8.0

**参考**：[http://php.net/manual/en/function.strlen.php](http://php.net/manual/en/function.strlen.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
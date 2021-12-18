# PHP|strtolower()函数

> Original: [https://www.geeksforgeeks.org/php-strtolower-function/](https://www.geeksforgeeks.org/php-strtolower-function/)

函数的作用是：将字符串转换为小写。 此函数接受字符串作为参数，并将字符串中出现的所有大写英语字母转换为小写。 字符串中的所有其他数字字符或特殊字符保持不变。

**语法**：

```
*string* strtolower( $string )

```

**参数**：此函数的唯一参数是要转换为小写的字符串。

**返回值**：此函数返回所有字母均为小写的字符串。

例如：

```
Input : $str  = "GeeksForGeeks"
        strtolower($str)
Output: geeksforgeeks

Input : $str  = "going BACK he SAW THIS 123$#%"
        strtolower($str)
Output: going back he saw this 123$#%

```

下面的程序演示了 PHP 中的 strtolower()函数：

**程序 1**：

```
<?php

// original string
$str = "GeeksForGeeks";

// string converted to lower case
$resStr = strtolower($str);

print_r($resStr);

?>
```

产出：

```
geeksforgeeks

```

**程序 2**：

```
<?php

// original string
$str = "going BACK he SAW THIS 123$#%";

// string converted to lower case
$resStr = strtolower($str);

print_r($resStr);

?>
```

产出：

```
going back he saw this 123$#%

```

**参考**：
[http://php.net/manual/en/function.strtolower.php](http://php.net/manual/en/function.strtolower.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
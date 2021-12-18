# PHP|str_rot13()函数

> Original: [https://www.geeksforgeeks.org/php-str_rot13-function/](https://www.geeksforgeeks.org/php-str_rot13-function/)

函数 str_rot13()是 php 中的内置函数。 此函数接受字符串，并将字符串中的每个字母在字母表中移位 13 位。 该函数保留数字和非字母字符不变。 通过将编码字符串作为参数传递，该函数将返回原始字符串。

**语法：**

```
str_rot13 ( $string )
```

**参数：**此函数仅接受从以上语法可以观察到的字符串参数。 参数说明如下。

*   **$string：**这是函数的唯一强制参数。 此参数将字符串传递给需要编码的函数。

**返回值：**该函数返回编码后的字符串。

例如：

```
Input : $string = "Geeks for Geeks"
Output : Trrxf sbe Trrxf

Input : $string = "Trrxf sbe Trrxf"
Output : Geeks for Geeks

```

下面的程序演示了 PHP 中的 str_rot13()函数：

```
<?php

echo str_rot13("Geeks for Geeks");
echo "\n";
echo str_rot13("Trrxf sbe Trrxf");

?>
```

发帖主题：Re：Колибри0.7.8.0

```
Trrxf sbe Trrxf
Geeks for Geeks
```

**引用：**
[http://php.net/manual/en/function.str-rot13.php](http://php.net/manual/en/function.str-rot13.php)
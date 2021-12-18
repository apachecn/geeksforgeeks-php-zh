# PHP|IntlChar tolower()函数

> Original: [https://www.geeksforgeeks.org/php-intlchartolower-function/](https://www.geeksforgeeks.org/php-intlchartolower-function/)

**IntlChar：：tolower()**函数是 PHP 中的内置函数，用于将字符转换为 Unicode 小写字符。 给定的输入字符被映射到其等效的小写字符。 如果字符没有小写等效项，则返回字符本身。

**语法：**

```
*mixed* IntlChar::tolower ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，这是必需的。 输入参数是一个字符，编码为 UTF-8 字符串。

**返回值：**此函数返回给定字符的小写映射字符。 如果字符没有小写映射字符，则返回自身。 返回类型将为 INTEGER，除非代码点作为 UTF-8 字符串传递，在这种情况下将返回字符串。

下面的程序演示了 PHP 中的**IntlChar：：tolower()**函数：

**程序 1：**

```
<?php

// PHP program to illustrate
// IntlChar::tolower function

// Input data is uppercase character symbol
var_dump(IntlChar::tolower("A"));

// Input data is lowercase character symbol
var_dump(IntlChar::tolower("a"));

// Input data is number symbol
var_dump(IntlChar::tolower("1"));

// Input data is string symbol
var_dump(IntlChar::tolower(ord("XYZ")));

// Input data is uppercase character symbol
var_dump(IntlChar::tolower(ord("I")));
?>
```

**输出：**

```
string(1) "a"
string(1) "a"
string(1) "1"
int(120)
int(105)

```

**程序 2：**

```
<?php
// PHP code to illustrate IntlChar::tolower()

// Declare an array $arr
$arr = array(ord("A"), "291", "^", "A", "a", "1");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::tolower($val));
}
?>
```

**输出：**

```
int(97)
NULL
string(1) "^"
string(1) "a"
string(1) "a"
string(1) "1"

```

**相关文章：**

*   [php|IntlChar：：isDown()函数](https://www.geeksforgeeks.org/php-intlcharislower-function/)
*   [php|IntlChar：：Isp()函数](https://www.geeksforgeeks.org/php-intlcharisupper-function/)

**引用：**[http://php.net/manual/en/intlchar.tolower.php](http://php.net/manual/en/intlchar.tolower.php)
# PHP|IntlChar Toupper()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-toupper-function/](https://www.geeksforgeeks.org/php-intlchar-toupper-function/)

**IntlChar：：Toupper()**函数是 PHP 中的内置函数，用于将字符转换为 Unicode 字符大写。 给定的字符将更改为其大写等效字符。 如果字符没有大写等效项，则返回相同的字符。

**语法：**

```
*mixed* IntlChar::toupper ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 整数*$CODEPOINT*的值是(例如，U+2603 雪人的值为 0x2603)，或编码为*UTF-8*字符串的字符(例如“\u{2603}”)。

**返回值：**此函数返回给定字符的大写映射字符。 如果给定字符没有大写映射字符，则返回字符本身。 返回类型将为 INTEGER，除非代码点作为 UTF-8 字符串传递，在这种情况下将返回字符串。

下面的程序演示了 PHP 中的**IntlChar：：Toupper()**函数：

**程序 1：**

```
<?php

// PHP program to illustrate
// IntlChar::toupper function

// Input data is uppercase character symbol
var_dump(IntlChar::toupper("A"));

// Input data is lowercase character symbol
var_dump(IntlChar::toupper("a"));

// Input data is number symbol
var_dump(IntlChar::toupper("1"));

// Input data is string symbol
var_dump(IntlChar::toupper(ord("xyz")));

// Input data is uppercase character symbol
var_dump(IntlChar::toupper(ord("I")));
?>
```

**输出：**

```
string(1) "A"
string(1) "A"
string(1) "1"
int(88)
int(73)

```

**程序 2：**

```
<?php
// PHP code to illustrate IntlChar::toupper()

// Declare an array $arr
$arr = array(ord("A"), "291", "^", "A", "a", "1");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::toupper($val));
}
?>
```

**输出：**

```
int(65)
NULL
string(1) "^"
string(1) "A"
string(1) "A"
string(1) "1"

```

**相关文章：**

*   [php|IntlChar：：isDown()函数](https://www.geeksforgeeks.org/php-intlcharislower-function/)
*   [php|IntlChar：：Isp()函数](https://www.geeksforgeeks.org/php-intlcharisupper-function/)

**引用：**[http://php.net/manual/en/intlchar.toupper.php](http://php.net/manual/en/intlchar.toupper.php)
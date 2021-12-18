# PHP|IntlChar getCombiningClass()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getcombiningclass-function/](https://www.geeksforgeeks.org/php-intlchar-getcombiningclass-function/)

**IntlChar：：getCombiningClass()**函数是 PHP 中的一个内置函数，用于获取代码点的组合类。
**语法：**

```
*int* IntlChar::getCombiningClass ( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。
**返回值：**此函数返回代码点的组合类。

下面的程序演示了 PHP 中的**IntlChar：：getCombiningClass()**函数：

**程序 1：**

## PHP

```
<?php

// PHP function to illustrate
// the use of IntlChar::getCombiningClass()

// Input data is string type
var_dump(IntlChar::getCombiningClass("\p{143}"));

// Input data is character type
var_dump(IntlChar::getCombiningClass(" "));

// Input data is unicode character type
var_dump(IntlChar::getCombiningClass("\u{350}"));

// Input data is string type
var_dump(IntlChar::getCombiningClass("XYZ"));

// Input data is unicode character type
var_dump(IntlChar::getCombiningClass("\u{0358}"));

?>
```

**Output:** 

```
NULL
int(0)
int(230)
NULL
int(232)

```
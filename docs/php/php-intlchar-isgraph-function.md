# PHP|IntlChar isgraph()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-isgraph-function/](https://www.geeksforgeeks.org/php-intlchar-isgraph-function/)

**IntlChar：：isgraph()**函数是 PHP 中的一个内置函数，用于检查代码点是否为图形字符。 对于除具有常规类别 CC(控制代码)、CF(格式控制)、Cs(代理)、CN(未分配)和 Z(分隔符)的字符以外的所有字符，它都返回 True。

**语法：**

```
*bool* IntlChar::isgraph ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为 UTF-8 字符串。

**返回值：**如果*$codepoint*是图形字符，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isgraph()**函数：

**程序 1：**

```
<?php

// PHP code to illustrate the 
// IntlChar::isgraph() function.

// Alphabet cases 
var_dump(IntlChar::isgraph("c"));

// Single digit
var_dump(IntlChar::isgraph("4"));

// UTF encoded string
var_dump(IntlChar::isgraph("\u{2403}"));

// new line character
var_dump(IntlChar::isgraph("\n"));

// vertical tab character
var_dump(IntlChar::isgraph("\t"));
?>
```

**输出：**

```
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)

```

**程序 2：**

```
<?php
// PHP code to illustrate IntlChar isgraph()

// Declare an array $arr
$arr = array("Z", "291", "^", "  ", "*", "Sudo Placement");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isgraph($val));
}
?>
```

**输出：**

```
bool(true)
NULL
bool(true)
NULL
bool(true)
NULL

```

**相关文章：**

*   [php|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)
*   [php|IntlChar：：isdigit()函数](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)

**引用：**[http://php.net/manual/en/intlchar.isgraph.php](http://php.net/manual/en/intlchar.isgraph.php)
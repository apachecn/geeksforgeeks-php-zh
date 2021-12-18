# PHP|IntlChar：：isIDStart()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisidstart-function/](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)

**IntlChar：：isIDStart()**函数是 PHP 中的一个内置函数，用于检查给定的输入字符代码点是否允许，因为第一个字符是标识符。 一般类别为“L”(字母)和“NL”(字母和数字)的字符为真。

**语法：**

```
bool IntlChar::isIDStart( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。

**返回值：**如果*$codepoint*以标识符字符开头，则返回 True，否则返回 False。

以下程序说明了 PHP 中的**IntlChar：：isIDStart()**函数：

**程序 1：**

## PHP

```
<?php
// PHP code to illustrate
// IntlChar::isIDStart() function

// Input character codepoint value
var_dump(IntlChar::isIDStart("G"));

// Input string codepoint value
var_dump(IntlChar::isIDStart("Geeks"));

// Input int codepoint value
var_dump(IntlChar::isIDStart("3 "));

// Input floating codepoint value
var_dump(IntlChar::isIDStart("2025.6003"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isIDStart("\u{007F}"));
var_dump(IntlChar::isIDStart("\u{012C}"));

// Input symbolic codepoint value
var_dump(IntlChar::isIDStart(" $ "));
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
NULL
NULL
NULL
bool(false)
bool(true)
NULL

```

**程序 2：**

## PHP

```
<?php
// PHP code to illustrate
// IntlChar::isIDStart() function
// Declare an array with
// different codepoint value
$arr = array("h",
             "H",
             ".",
             "999",
             "\n",
             " ",
             "\u{007F}"
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isIDStart($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
bool(true)
bool(false)
NULL
bool(false)
bool(false)
bool(false)

```

**相关文章：**

*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isUWhiteSpace()函数](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)
*   [IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)

**引用：**[http://php.net/manual/en/intlchar.isidstart.php](http://php.net/manual/en/intlchar.isidstart.php)
# PHP|IntlChar：：isIDPart()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisidpart-function/](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)

**IntlChar：：isIDPart()**函数是 PHP 中的内置函数，用于检查给定的输入字符在标识符中是否允许。 对于一般类别为“L”(字母)、“ND”(十进制数字)、“NL”(字母数字)、“Mc”和“Mn”(组合符号)、“Pc”(连接标点符号)和 u_isIDIgnorable(C)的字符为 True。
**语法：**和

```php
*bool* IntlChar::isIDPart( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为 UTF-8 字符串。
**返回值：**如果*$CODEPOINT*是标识符字符，则返回 True，否则返回 False。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：isIDPart()**函数

## PHP

```php
<?php

// PHP code to illustrate
// IntlChar::isIDPart() function

// Input character codepoint value
var_dump(IntlChar::isIDPart("X"));

// Input string codepoint value
var_dump(IntlChar::isIDPart("Geeks"));

// Input symbolic codepoint value
var_dump(IntlChar::isIDPart("^ "));

// Input int codepoint value
var_dump(IntlChar::isIDPart("3 "));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isIDPart("\u{007F}"));
var_dump(IntlChar::isIDPart("\u{012C}"));
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
bool(true)
NULL
NULL
NULL
bool(true)
bool(true)
```

**程序 2：**

## PHP

```php
<?php
// PHP code to illustrate
// IntlChar::isIDPart() function
// Declare an array with
// different codepoint value
$arr = array("D",
            "\u{007F}",
            ".",
            "8",
            "/",
            " "
      );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isIDPart($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
bool(true)
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)
```

**相关文章：**和

*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isUWhiteSpace()函数](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)
*   [IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)
*   [IntlChar：：isUUppercase()函数](https://www.geeksforgeeks.org/php-intlcharisuuppercase-function/)

**引用：**[http://php.net/manual/en/intlchar.isidpart.php](http://php.net/manual/en/intlchar.isidpart.php)
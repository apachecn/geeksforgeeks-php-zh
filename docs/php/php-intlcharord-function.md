# PHP|IntlChar：：Ord()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharord-function/](https://www.geeksforgeeks.org/php-intlcharord-function/)

**IntlChar：：Ord()**函数是 PHP 中的内置函数，用于返回给定字符的 Unicode 码点值。

**语法：**

```
*int* IntlChar::ord( $character )
```

**参数：**此函数接受单个参数*$character*，该参数是必需的。 此参数是 Unicode 字符。
**返回值：**返回 Unicode 码点值，整型。

下面的程序演示了 PHP 中的**IntlChar：：Ord()**函数：

**程序 1：**

## PHP

```
<?php
// PHP function to illustrate
// the use of IntlChar::ord()

// Input int codepoint value
var_dump(IntlChar::ord("4"));

// Input character codepoint value
var_dump(IntlChar::ord("B"));

// Input character codepoint value
var_dump(IntlChar::ord("b"));

//Input int codepoint value
var_dump(IntlChar::ord("2018"));

// Input character codepoint value
var_dump(IntlChar::ord("Geeks"));

// Input symbole codepoint value
var_dump(IntlChar::ord("@"));

// Input symbole codepoint value
var_dump(IntlChar::ord("*"));

// Input space codepoint value
var_dump(IntlChar::ord(" "));
?>
```

发帖主题：Re：Колибри0.7.0

```
int(52)
int(66)
int(98)
NULL
NULL
int(64)
int(42)
int(32)
```

**程序 2：**

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::ord()

// Declare an array with
// different codepoint value
$arr = array("X",
            "x",
            "*",
            "8",
            "0",
            " ", 
            "&",
            ")",
            "99",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::ord($val));
}
?>           
```

发帖主题：Re：Колибри0.7.0

```
int(88)
int(120)
int(42)
int(56)
int(48)
int(32)
int(38)
int(41)
NULL
```

**相关文章：**

*   [order()函数](https://www.geeksforgeeks.org/php-ord-function/)
*   [IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)
*   [IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)

**引用：**[http://php.net/manual/en/intlchar.ord.php](http://php.net/manual/en/intlchar.ord.php)
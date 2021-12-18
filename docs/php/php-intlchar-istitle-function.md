# PHP|IntlChar istitle()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-istitle-function/](https://www.geeksforgeeks.org/php-intlchar-istitle-function/)

**IntlChar：：istitle**函数是 PHP 中的一个内置函数，用于检查输入的字符代码点是否为大小写字母。 在 True 案例中，具有一般类别的字符是“lt”(大写字母)。
**语法：**和

```
*bool* IntlChar::istitle( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数*$codepoint*是一个字符或整数值，编码为 UTF-8 字符串。
**返回值：**如果*$codepoint*是大小写字母，则返回 True，否则返回 False。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：istitle()**函数

## PHP

```
<?php
// PHP function to illustrate the
//use of IntlChar::istitle()

// Input Capital letter  codepoint
var_dump(IntlChar::istitle("Welcome to Geeks"));

// Input Capital letter  codepoint
var_dump(IntlChar::istitle("\u{03A6}"));

// Input Capital letter  codepoint
var_dump(IntlChar::istitle("?"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::istitle("\u{00A0}"));

// Input symbolic space codepoint value
var_dump(IntlChar::istitle(" "));

// Input symbolic codepoint value
var_dump(IntlChar::istitle(" ^ "));

// Input int codepoint value
var_dump(IntlChar::istitle("3"));

?>
```

**Output:** 

```
NULL
bool(false)
bool(false)
bool(false)
bool(false)
NULL
bool(false)
```

**程序 2：**和

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::istitle()

// Declare an array with
// different codepoint value
$arr = array("G",
             "\u{03C6}",
             "\t",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::istitle($val));
}
?>
```

**Output:** 

```
bool(false)
bool(false)
bool(false)
```

**引用：**[https://www.php.net/manual/en/intlchar.istitle.php](https://www.php.net/manual/en/intlchar.istitle.php)
# PHP|IntlChar：：isUAlphabetic()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisualphabetic-function/](https://www.geeksforgeeks.org/php-intlcharisualphabetic-function/)

**IntlChar：：isUAlphabetic()**函数是 PHP 中的内置函数，用于检查给定的输入字符是否为字母 Unicode 字符。

**语法：**

```
*bool* IntlChar::isUAlphabetic( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是整数或字符，编码为*UTF-8*字符串。

**返回值：**如果*$codepoint*是字母 Unicode 字符，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isUAlphabetic()**函数：

**程序 1：**

## PHP

```
<?php
// PHP program to illustrate
// IntlChar::isUAlphabetic() function

// Input data is character type
var_dump(IntlChar::isUAlphabetic("G"));

// Input data is string type
var_dump(IntlChar::isUAlphabetic("B\n"));

// Input data is string type
var_dump(IntlChar::isUAlphabetic("Geeksforgeeks"));

// Input data is number(multiple digit)
var_dump(IntlChar::isUAlphabetic("2018"));

// Input data is single digit
var_dump(IntlChar::isUAlphabetic("9"));

// Input data is floating point number
var_dump(IntlChar::isUAlphabetic("10.99"));

?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
NULL
NULL
NULL
bool(false)
NULL

```

**程序 2：**

## PHP

```
<?php
// PHP code to illustrate IntlChar::isUAlphabetic()

// Declare an array $arr
$arr = array("Z", "291", "^", "  ", "*", "Sudo Placement");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isUAlphabetic($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
NULL
bool(false)
NULL
bool(false)
NULL

```

**相关文章：**

*   [PHP|IntlChar：：isUUppercase()函数](https://www.geeksforgeeks.org/php-intlcharisuuppercase-function/)
*   [PHP|IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)
*   [PHP|IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)
*   [PHP|IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)

**引用：**[http://php.net/manual/en/intlchar.isualphabetic.php](http://php.net/manual/en/intlchar.isualphabetic.php)
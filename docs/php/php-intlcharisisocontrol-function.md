# PHP|IntlChar：：isISOControl()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisisocontrol-function/](https://www.geeksforgeeks.org/php-intlcharisisocontrol-function/)

**IntlChar：：isISOControl()**函数是 PHP 中的内置函数，用于检查输入代码点是否为 ISO 控制代码字符。 要确定码位是否为 ISO 控制码的指定码位。 一般类别“CC”为 U+0000…为真。 U+001f 和 U+007f…。 U+009F。

**语法：**

```php
*bool* IntlChar::isISOControl( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。

**返回值：**如果*$codepoint*是 ISO 控制代码字符，则返回 True，否则返回 False。

**注：**如果输入码点参数为字符串和数字，则返回 NULL。

以下程序说明了 PHP 中的**IntlChar：：isISOControl()**函数：

**程序 1：**

## PHP

```php
<?php
// PHP code to illustrate
// IntlChar::isISOControl() function

// Input control with double " "
// character codepoint value
var_dump(IntlChar::isISOControl("\n"));

// Input control with single ''
// character codepoint value
var_dump(IntlChar::isISOControl('\n'));

// Input string codepoint value
var_dump(IntlChar::isISOControl("Sudo\tPlacement"));

// Input int codepoint value
var_dump(IntlChar::isISOControl("3 "));

// Input int codepoint value
var_dump(IntlChar::isISOControl("1\n2\n3\n4\n "));

// Input floating codepoint value
var_dump(IntlChar::isISOControl("33.44"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isISOControl("\u{007F}"));

// Input symbolic codepoint value
var_dump(IntlChar::isISOControl(" @ "));
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
NULL
NULL
NULL
NULL
NULL
bool(true)
NULL

```

**程序 2：**

## PHP

```php
<?php
// PHP code to illustrate
// IntlChar::isISOControl() function
// Declare an array with
// different codepoint value
$arr = array("\r",
             ".",
             " ",
             "\n",
             "\u",
             " ",
             "\t",
             "\\",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isISOControl($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
bool(false)
bool(false)
bool(true)
NULL
bool(false)
bool(true)
bool(false)

```

**相关文章：**

*   [IntlChar：：isUWhiteSpace()函数](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)
*   [IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)
*   [IntlChar：：isUUppercase()函数](https://www.geeksforgeeks.org/php-intlcharisuuppercase-function/)

**引用：**[http://php.net/manual/en/intlchar.isisocontrol.php](http://php.net/manual/en/intlchar.isisocontrol.php)
# PHP|IntlChar：：isIDIgnorable()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisidignorable-function/](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)

**IntlChar：：isIDIgnorable()**函数是 PHP 中的内置函数，用于确定代码点是否为可以忽略的字符。 对于一般类别为“CF”(格式控件)的字符以及非空格 ISO 控件(U+00000…)也是如此。 U+0008、U+000E…。 U+001B，U+007F…。 U+009F)。

**语法：**

```php
*bool* IntlChar::isIDIgnorable( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 它是一个字符或整数值，编码为 UTF-8 字符串。

**返回值：**如果*$codepoint*是可以忽略的标识符，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isIDIgnorable()**函数。
**程序 1：**

```php
<?php

// PHP code to illustrate
// IntlChar::isIDIgnorable() function

// Input character codepoint value 
var_dump(IntlChar::isIDIgnorable("X"));
echo "<br>";

// Input symbolic codepoint value 
var_dump(IntlChar::isIDIgnorable("^ "));
echo "<br>";

// Input int codepoint value 
var_dump(IntlChar::isIDIgnorable("3 "));
echo "<br>";

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isIDIgnorable("\u{007F}"));
echo "<br>";

var_dump(IntlChar::isIDIgnorable("\u{012C}"));
echo "<br>";

// Input string codepoint value 
var_dump(IntlChar::isIDIgnorable("Geeks"));
echo "<br>";

?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
NULL
NULL
bool(true)
bool(false)
NULL

```

**程序 2：**

```php
<?php

// PHP code to illustrate
// IntlChar::isIDIgnorable function

// Declare an array $arr
$arr = array("G", "\u{007F}", ".", "8", "/",
              "\u{000}", "\t", "\u{007}", "\u{0AB}" );

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isIDIgnorable($val));
    echo "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
bool(true)
bool(false)
bool(false)
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)

```

**相关文章：**

*   [IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)
*   [IntlChar：：isalpha()函数](https://www.geeksforgeeks.org/php-intlcharisalpha-function/)
*   [IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)

**引用：**[http://php.net/manual/en/intlchar.isidignorable.php](http://php.net/manual/en/intlchar.isidignorable.php)
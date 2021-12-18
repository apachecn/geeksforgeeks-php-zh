# PHP|IntlChar：：isUWhiteSpace()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)

**IntlChar：：isUWhiteSpace()**函数是 PHP 中的内置函数，用于检查给定的输入字符是否为空白 Unicode 字符。 IntlChar 访问数字实用程序函数，并用于访问有关 Unicode 字符的信息。
**语法：**和

```php
*bool* IntlChar::isUWhiteSpace( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。
**返回值：**如果*$codepoint*为空白字符，则返回 True，否则返回 False。
下面的程序说明了 PHP 中的**IntlChar：：isUWhiteSpace()**函数。
**程序 1：**和

## PHP

```php
<?php
// PHP code to illustrate IntlChar::isUWhiteSpace()
// function

// Input Capital Letter
var_dump(IntlChar::isUWhiteSpace("N"));

// Input Small Letter
var_dump(IntlChar::isUWhiteSpace(" n "));

// Input Whitesapce Character  "\n "
var_dump(IntlChar::isUWhiteSpace("\n"));

// Input encoded string
var_dump(IntlChar::isUWhiteSpace("\u{00B0}"));
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
bool(false)
NULL
bool(true)
bool(false)
```

**程序 2：**和

## PHP

```php
<?php
// PHP code to IntlChar::isUWhiteSpace()
// function

// Declare an array $arr
$arr = array("X\t", "\n", "^", "\r", "\t\r");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isUWhiteSpace($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
NULL
bool(true)
bool(false)
bool(true)
NULL
```

**相关文章：**和

*   [PHP|IntlChar：：isUUppercase()函数](https://www.geeksforgeeks.org/php-intlcharisuuppercase-function/)
*   [PHP|IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)
*   [PHP|IntlChar：：charName()函数](https://www.geeksforgeeks.org/php-intlcharcharname-function/)

**引用：**[http://php.net/manual/en/intlchar.isuwhitespace.php](http://php.net/manual/en/intlchar.isuwhitespace.php)
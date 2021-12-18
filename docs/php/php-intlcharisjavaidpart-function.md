# PHP|IntlChar：：isJavaIDPart()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisjavaidpart-function/](https://www.geeksforgeeks.org/php-intlcharisjavaidpart-function/)

**IntlChar：：isJavaIDPart()**函数是 PHP 中的一个内置函数，用于检查 Java 标识符中是否允许输入代码点。 要确定码位是否为 Java 标识符的指定码位。 添加了[isIDPart()](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)函数的一般类别“SC”(货币符号)为 True。
**语法：**和

```php
*bool* IntlChar::isJavaIDPart( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数*$codepoint*是一个字符或整数值，编码为 UTF-8 字符串。
**返回值：**如果*$codepoint*是 Java 标识符字符，则返回 True，否则返回 False。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：isJavaIDPart()**函数

## PHP

```php
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaIDPart()

// Input control character codepoint value
var_dump(IntlChar::isJavaIDPart("\n"));

// Input string codepoint value
var_dump(IntlChar::isJavaIDPart("Report Bug"));

// Input int codepoint value
var_dump(IntlChar::isJavaIDPart("3 "));

// Input string codepoint value
var_dump(IntlChar::isJavaIDPart("R"));

// Input floating codepoint value
var_dump(IntlChar::isJavaIDPart("33.44"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isJavaIDPart("\u{007F}"));

// Input symbolic codepoint value
var_dump(IntlChar::isJavaIDPart(" @ "));
var_dump(IntlChar::isJavaIDPart(" $ "));

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
bool(false)
NULL
NULL
bool(true)
NULL
bool(true)
NULL
NULL
```

**程序 2：**

## PHP

```php
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaIDPart()

// Declare an array with
// different codepoint value
$arr = array("\r",
             "R",
             " ",
             "\u",
             " 5",
             "\t",
             "Geeks",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isJavaIDPart($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
bool(false)
bool(true)
bool(false)
NULL
NULL
bool(false)
NULL
```

**相关文章：**和

*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)
*   [IntlChar：：isIDPart()函数](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)

**引用：**[http://php.net/manual/en/intlchar.isjavaidpart.php](http://php.net/manual/en/intlchar.isjavaidpart.php)
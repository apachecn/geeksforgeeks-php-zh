# PHP|IntlChar isMirrored()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-ismirrored-function/](https://www.geeksforgeeks.org/php-intlchar-ismirrored-function/)

**IntlChar：：isMirrored()**函数是 PHP 中的一个内置函数，用于检查代码点是否包含 BIDI_MIRRORED 属性。 此属性用于设置从右向左上下文中常用且需要用镜像图形显示的字符。

**语法：**

```php
*bool* IntlChar::isMirrored ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数为整数值或字符，编码为 UTF-8 字符串。

**返回值：**如果*$codepoint*具有 BIDI_MIRRORED 属性，则此函数返回 True，否则返回 False。

以下程序说明了 PHP 中的**IntlChar：：isMirrored()**函数：

**程序 1：**

```php
<?php

// PHP program to illustrate
// IntlChar::isMirrored function

// Input data is character type
var_dump(IntlChar::isMirrored("A"));

// Input character symbol
var_dump(IntlChar::isMirrored("<"));

// Input character symbol
var_dump(IntlChar::isMirrored("("));

// Input character symbol
var_dump(IntlChar::isMirrored("^"));
?>
```

**输出：**

```php
bool(false)
bool(true)
bool(true)
bool(false)

```

**程序 2：**

```php
<?php
// PHP code to illustrate IntlChar::isMirrored()
// function.

// Declare an array $arr
$arr = array("Z", "291", "^", "A", "<", ")");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isMirrored($val));
}
?>
```

**输出：**

```php
bool(false)
NULL
bool(false)
bool(false)
bool(true)
bool(true)

```

**相关文章：**

*   [php|IntlChar：：charMirror()函数](https://www.geeksforgeeks.org/php-intlcharcharmirror-function/)
*   [php|IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)
*   [php|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)

**引用：**[http://php.net/manual/en/intlchar.ismirrored.php](http://php.net/manual/en/intlchar.ismirrored.php)
# PHP|IntlChar：：isULowercase()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisulowercase-function/](https://www.geeksforgeeks.org/php-intlcharisulowercase-function/)

**IntlChar：：isULowercase()**函数是 PHP 中的内置函数，用于检查给定的输入字符是否为小写字符。
**语法：**

```php
*bool* IntlChar::isULowercase( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。
**返回值：**如果$codepoint 是小写 Unicode 字符，则返回 True，否则返回 False。
**注意：**此函数与*IntlChar：：islow()*函数不同。
下面的程序说明了**IntlChar：：isULowercase()**函数是 PHP 中的一个内置函数，用于检查给定的输入字符是否为小写字符。

**语法：**

```php
bool IntlChar::isULowercase( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。
**返回值：**如果$codepoint 是小写 Unicode 字符，则返回 True，否则返回 False。
**注意：**此函数与*IntlChar：：islow()*函数不同。
下面的程序说明了 PHP：
**程序 1 中的 IntlChar：：isULowercase()函数。**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::isULowercase()()
// function

// Input data is Capital letter or character
var_dump(IntlChar::isULowercase("M"));

// Input data is small letter or character
var_dump(IntlChar::isULowercase("m"));

// Input data is Capital letter string
var_dump(IntlChar::isULowercase("GEEKS"));

// Input data is small letter string
var_dump(IntlChar::isULowercase("geeks"));

// Input data is integer value
var_dump(IntlChar::isULowercase("7"));
?>
```

**输出：**

```php
bool(false)
bool(true)
NULL
NULL
bool(false)
```

**程序 2：**

## PHP

```php
<?php

// PHP code to IntlChar::isULowercase()
// function

// Declare an array $arr
$arr = array("G", "Sudo", "^", "s", "6", "\n");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isULowercase($val));
}
?>
```

**输出：**

```php
bool(false) 
NULL 
bool(false) 
bool(true) 
bool(false) 
bool(false)
```

**相关文章：**

*   [**PHP|IntlChar：：isUAlphabetic()函数**](https://www.geeksforgeeks.org/php-intlcharisualphabetic-function/)
*   [**PHP|IntlChar：：isUWhiteSpace()函数**](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)

**引用：**[php 中的 http://php.net/manual/en/intlchar.isulowercase.php](http://php.net/manual/en/intlchar.isulowercase.php)rcase()函数：

**程序 1：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::isULowercase()
// function

// Input data is Capital letter or character
var_dump(IntlChar::isULowercase("M"));

// Input data is small letter or character
var_dump(IntlChar::isULowercase("m"));

// Input data is Capital letter string
var_dump(IntlChar::isULowercase("GEEKS"));

// Input data is small letter string
var_dump(IntlChar::isULowercase("geeks"));

// Input data is integer value
var_dump(IntlChar::isULowercase("7"));
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
bool(true)
NULL
NULL
bool(false)
```

**程序 2：**

## PHP

```php
<?php

// PHP code to IntlChar::isULowercase()
// function

// Declare an array $arr
$arr = array("G", "Sudo", "^", "s", "6", "\n");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isULowercase($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false) 
NULL 
bool(false) 
bool(true) 
bool(false) 
bool(false) 
```

**相关文章：**

*   [PHP|IntlChar：：isUAlphabetic()函数](https://www.geeksforgeeks.org/php-intlcharisualphabetic-function/)
*   [PHP|IntlChar：：isUWhiteSpace()函数](https://www.geeksforgeeks.org/php-intlcharisuwhitespace-function/)

**引用：**[http://php.net/manual/en/intlchar.isulowercase.php](http://php.net/manual/en/intlchar.isulowercase.php)
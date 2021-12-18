# PHP|IntlChar：：isalpha()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisalpha-function/](https://www.geeksforgeeks.org/php-intlcharisalpha-function/)

**IntlChar：：isalpha()**函数是 PHP 中的一个内置函数，用于检查给定的输入是否为字母数字字符。

**语法：**

```php
*bool* IntlChar::isalpha( $codepoint )
```

**参数：**IntlChar：：isalpha()函数接受单个参数*$codepoint*，这是必需的。 输入参数是整数值或字符，编码为*UTF-8*字符串。
**返回值：**如果$codepoint 是字母数字字符，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isalpha()**函数：

**程序 1：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::isalpha()
// function

// Input data is character type
var_dump(IntlChar::isalpha("G"));

// Input data is string type
var_dump(IntlChar::isalpha("G\n"));

// Input data is string type
var_dump(IntlChar::isalpha("Geeksforgeeks"));

// Input data is number
var_dump(IntlChar::isalpha("2018"));

// Input data is single digit
var_dump(IntlChar::isalpha("5"));
?>
```

**输出：**

```php
bool(true) 
NULL 
NULL 
NULL 
bool(false)
```

**程序 2：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::isalpha()

// Declare an array $arr
$arr = array("G", "GeeksforGeeks", "^", "1001", "6", "\u{2018}");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isalpha($val));
}
?>
```

**输出：**

```php
bool(true) 
NULL 
bool(false) 
NULL 
bool(false) 
bool(false) 
```

**相关文章：**

*   [PHP|IntlChar：：isdigit()函数](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)
*   [PHP|IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)
*   [PHP|IntlChar：：isbase()函数](https://www.geeksforgeeks.org/php-intlcharisbase-function/)

**引用：**[http://php.net/manual/en/intlchar.isalpha.php](http://php.net/manual/en/intlchar.isalpha.php)
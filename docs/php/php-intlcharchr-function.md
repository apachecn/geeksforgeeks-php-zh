# PHP|IntlChar：：CHR()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharchr-function/](https://www.geeksforgeeks.org/php-intlcharchr-function/)

**IntlChar：：Chr()**函数是 PHP 中的一个内置函数，用于检查给定的输入字符是否为 Unicode 代码点值。 它按代码点值返回 Unicode 字符。
**语法：**和

```php
*string* IntlChar::chr( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。
**返回值：**在 True 情况下，*$CODEPOINT*字符串包含由 Unicode 代码点值指定的单个字符，否则返回 NULL。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：Chr()**函数

## PHP

```php
<?php
// PHP function to illustrate
// the use of IntlChar::chr()

// Input int codepoint value
var_dump(IntlChar::chr(" "));

// Input int codepoint value
var_dump(IntlChar::chr(101));

// Input char codepoint value
var_dump(IntlChar::chr("G"));

// Input char  codepoint value
var_dump(IntlChar::chr("Geeks"));

// Input Symbolic codepoint value
var_dump(IntlChar::chr("{content}quot;));

// Input Symbolic codepoint value
var_dump(IntlChar::chr("#"));

// Input Symbolic codepoint value
var_dump(IntlChar::chr("@"));

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
string(1) " " 
string(1) "e" 
string(1) "G" 
NULL 
string(1) "{content}quot; 
string(1) "#" 
string(1) "@" 
```

**程序 2：**和

## PHP

```php
<?php
// PHP function to illustrate the
// use of IntlChar::chr

// Declare an array with
// different codepoint value
$arr = array("D",
            ("E"),
             77,
            123,
            65,
            97,

        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::chr($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
string(1) "D" 
string(1) "E" 
string(1) "M"  
string(1) "{" 
string(1) "A" 
string(1) "a" 
```

**相关文章：**和

*   [PHP|chr()函数](https://www.geeksforgeeks.org/php-chr-fucntion/)
*   [IntlChar：：isWhitespace()函数](https://www.geeksforgeeks.org/php-intlchariswhitespace-function/)
*   [IntlChar：：isUUppercase()函数](https://www.geeksforgeeks.org/php-intlcharisuuppercase-function/)

**引用：**[http://php.net/manual/en/intlchar.chr.php](http://php.net/manual/en/intlchar.chr.php)
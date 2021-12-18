# PHP|IntlChar getFC_NFKC_Closure()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getfc_nfkc_closure-function/](https://www.geeksforgeeks.org/php-intlchar-getfc_nfkc_closure-function/)

**IntlChar：：getFC_NFKC_CLOSURE()**函数是 PHP 中的内置函数，用于获取代码点的 FC_NFKC_CLOSURE 属性。 此函数返回代码点的 FC_NFKC_CLOSURE 属性字符串。 如果代码点为 None，则返回空字符串。

**语法：**

```php
*string* IntlChar::getFC_NFKC_Closure( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**此函数返回代码点的 FC_NFKC_CLOSE 属性字符串，如果没有，则返回空字符串。

下面的程序演示了 PHP 中的**IntlChar：：getFC_NFKC_Closure()**函数：

**程序 1：**

```php
<?php

// PHP function to illustrate 
// the use of IntlChar::getFC_NFKC_Closure()

// Input data is unicode character type
var_dump(IntlChar::getFC_NFKC_Closure("\u{2121}"));

// Input data is unicode character type
var_dump(IntlChar::getFC_NFKC_Closure("\u{1D2D}"));

// Input data is string type
var_dump(IntlChar::getFC_NFKC_Closure("\p{143}"));

// Input data is character type
var_dump(IntlChar::getFC_NFKC_Closure(" "));

// Input data is unicode character type
var_dump(IntlChar::getFC_NFKC_Closure("\u{350}"));

// Input data is string type
var_dump(IntlChar::getFC_NFKC_Closure("XYZ"));

// Input data is unicode character type
var_dump(IntlChar::getFC_NFKC_Closure("\u{0358}"));

?>
```

**输出：**

```php
string(3) "tel"
string(2) "Ã¦"
NULL
string(0) ""
string(0) ""
NULL
string(0) ""

```

**程序 2：**

```php
<?php
// PHP code to illustrate getFC_NFKC_Closure()

// Declare an array $arr
$arr = array("\u{2121}", "\u{1D2D}", " ", "\u{350}", "XYZ", "G",
                "GeeksforGeeks", "^");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::getFC_NFKC_Closure($val));
}
?>
```

**输出：**

```php
string(3) "tel"
string(2) "Ã¦"
string(0) ""
string(0) ""
NULL
string(0) ""
NULL
string(0) ""

```

**相关文章：**

*   [php|IntlChar：：Ord()函数](https://www.geeksforgeeks.org/php-intlcharord-function/)
*   [php|IntlChar Toupper()函数](https://www.geeksforgeeks.org/php-intlchar-toupper-function/)
*   [php|IntlChar isgraph()函数](https://www.geeksforgeeks.org/php-intlchar-isgraph-function/)

**引用：**[http://php.net/manual/en/intlchar.getfc-nfkc-closure.php](http://php.net/manual/en/intlchar.getfc-nfkc-closure.php)
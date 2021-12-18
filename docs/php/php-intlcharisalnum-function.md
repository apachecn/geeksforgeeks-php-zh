# PHP|IntlChar：：isalnum()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisalnum-function/](https://www.geeksforgeeks.org/php-intlcharisalnum-function/)

**IntlChar：：isalnum()**函数是 PHP 中的一个内置函数，用于检查给定的输入是否为字母数字字符(数字或字母)。 对于具有常规类别“L”(字母)和“ND”(十进制数字)的字符，它返回 TRUE。

**语法：**

```
*bool* IntlChar::isalnum( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，这是必需的。 输入参数是整数值或字符，编码为*UTF-8*字符串。

**返回值：**如果$codepoint 是字母数字字符，则返回 True，否则返回 False。

**程序 1：**

## PHP

```
<?php

// PHP code to illustrate IntlChar::isalnum()
// Function

// Input data is character type
var_dump(IntlChar::isalnum("D"));

// Input data is string type
var_dump(IntlChar::isalnum("Geeksforgeeks"));

// Input data is integer type
var_dump(IntlChar::isalnum("234"));

// Input data is special character type
var_dump(IntlChar::isalnum("*"));

?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(true) 
NULL 
NULL 
bool(false) 
```

**程序 2：**

## PHP

```
<?php
// PHP code to illustrate IntlChar::isalnum()
// function

// Declare an array $arr
$arr = array("4", "20001111", "^", "  ", "*", "GeeksforGeeks");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isalnum($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(true) 
NULL 
bool(false) 
NULL 
bool(false) 
NULL 
```

**相关文章：**

*   [PHP|IntlChar：：isalpha()函数](https://www.geeksforgeeks.org/php-intlcharisalpha-function/)
*   [PHP|IntlChar：：isdigit()函数](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)
*   [PHP|IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)
*   [PHP|IntlChar：：isbase()函数](https://www.geeksforgeeks.org/php-intlcharisbase-function/)

**引用：**[http://php.net/manual/en/intlchar.isalnum.php](http://php.net/manual/en/intlchar.isalnum.php)
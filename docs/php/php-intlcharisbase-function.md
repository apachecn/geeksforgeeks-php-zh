# PHP|IntlChar：：isbase()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisbase-function/](https://www.geeksforgeeks.org/php-intlcharisbase-function/)

**IntlChar：：isbase()**函数是 PHP 中的内置函数，用于检查给定的输入数据是否为基本字符。 如果指定的代码点是基本字符，则对于常规类别“L”(字母)、“N”(数字)、“Mc”(空格组合标记)和“Me”(封闭标记)，它返回 TRUE。
**语法：**和

```php
*bool* IntlChar::isbase( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是整数或字符，编码为*UTF-8*字符串。
**返回值：**如果$codepoint 是基字符，则返回 TRUE，否则返回 FALSE。
示例：

```php
Input :(IntlChar::isbase("D"))
Output : bool(true)

Input : (IntlChar::isbase("*"))
Output : bool(false)

Input :(IntlChar::isbase("9"));
Output :bool(true)
```

以下程序说明 PHP：
**程序 1：**
中的**IntlChar：：isbase()**函数

## PHP

```php
<?php

// PHP code to illustrate IntlChar::isbase()
// Function

// Input data is character type
var_dump(IntlChar::isbase("D"));

// Input data is string type
var_dump(IntlChar::isbase("Geeksforgeeks"));

// Input data is integer type
var_dump(IntlChar::isbase("234"));

// Input data is special character type
var_dump(IntlChar::isbase("*"));

?>
```

输出：0

```php
bool(true) 
NULL 
NULL 
bool(false) 
```

**程序 2：**和

## PHP

```php
<?php
//PHP code to illustrate IntlChar::isbase()()

// Declare an array $arr
$arr = array("4", "20001111", "^", "  ", "*", "GeeksforGeeks");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isbase($val));
}
?>
```

输出：0

```php
bool(true) 
NULL 
bool(false) 
NULL 
bool(false) 
NULL 
```

**相关文章：**和

*   [PHP|IntlChar：：isdigit()函数](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)
*   [PHP|IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)

**引用：**[http://php.net/manual/en/intlchar.isbase.php](http://php.net/manual/en/intlchar.isbase.php)
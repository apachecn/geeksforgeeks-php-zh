# PHP|IntlChar getBlockCode()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getblockcode-function/](https://www.geeksforgeeks.org/php-intlchar-getblockcode-function/)

**IntlChar：：getBlockCode()**函数是 PHP 中的内置函数，用于获取包含代码点的 Unicode 分配块。 此函数返回包含字符的 Unicode 分配块。

**语法：**

```php
*int* IntlChar::getBlockCode ( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**此函数返回*$codepoint*的块值。 下面列出了一些码点的块值：

*   IntlChar：：BLOCK_CODE_BASIC_ 拉丁语
*   IntlChar：：Block_Code_ 希腊语
*   IntlChar：：Block_Code_Missing_Symbols

下面的程序演示了 PHP 中的**IntlChar：：getBlockCode()**函数：

**程序 1：**

## PHP

```php
<?php

// PHP function to illustrate
// the use of IntlChar::getBlockCode()

// Input data is character type
var_dump(IntlChar::getBlockCode("G") ===
          IntlChar::BLOCK_CODE_BASIC_LATIN);

// Input data is string type
var_dump(IntlChar::getBlockCode("ABC") ===
          IntlChar::BLOCK_CODE_BASIC_LATIN);

// Input data is character type
var_dump(IntlChar::getBlockCode("*") ===
               IntlChar::BLOCK_CODE_GREEK);

// Input data is unicode character type
var_dump(IntlChar::getBlockCode("\u{2603}") ===
     IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS);

// Input data is character type
var_dump(IntlChar::getBlockCode("@") ===
                     IntlChar::BLOCK_CODE_GREEK);
?>
```

**Output:** 

```php
bool(true)
bool(false)
bool(false)
bool(true)
bool(false)

```

**程序 2：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::getBlockCode()

// Declare an array $arr
$arr = array("G", "GeeksforGeeks", "^", "1001", "6", "\n");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::getBlockCode($val));
}
?>
```

**Output:** 

```php
int(1)
NULL
int(1)
NULL
int(1)
int(1)

```

**相关文章：**

*   [PHP|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)
*   [PHP|IntlChar：：totitle()函数](https://www.geeksforgeeks.org/php-intlchartotitle-function/)
*   [PHP|IntlChar charType()函数](https://www.geeksforgeeks.org/php-intlchar-chartype-function/)

**引用：**[http://php.net/manual/en/intlchar.getblockcode.php](http://php.net/manual/en/intlchar.getblockcode.php)
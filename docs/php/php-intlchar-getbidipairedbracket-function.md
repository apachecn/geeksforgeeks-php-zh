# PHP|IntlChar getBidiPairedBracket()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getbidipairedbracket-function/](https://www.geeksforgeeks.org/php-intlchar-getbidipairedbracket-function/)

**IntlChar：：getBidiPairedBracket()**函数是 PHP 中的内置函数，用于获取代码点的成对括号字符。 此函数使用配对的方括号进行映射。 如果字符没有对括号，则返回字符本身。

**语法：**

```php
IntlChar::getBidiPairedBracket ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，这是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**此函数返回映射的成对括号。 如果字符没有对括号，则返回字符本身。

下面的程序演示了 PHP 中的**IntlChar：：getBidiPairedBracket()**函数：

**程序 1：**

```php
<?php

// PHP function to illustrate 
// the use of IntlChar::getBidiPairedBracket()

// Input data is number type
var_dump(IntlChar::getBidiPairedBracket(91));

// Input data is bracket character type
var_dump(IntlChar::getBidiPairedBracket('['));

// Input data is bracket character type
var_dump(IntlChar::getBidiPairedBracket('}'));

// Input data is bracket character type
var_dump(IntlChar::getBidiPairedBracket('"'));

// Input data is string type
var_dump(IntlChar::getBidiPairedBracket('ABC'));

// Input data is character type
var_dump(IntlChar::getBidiPairedBracket('A'));
?>
```

**输出：**

```php
int(93)
string(1) "]"
string(1) "{"
string(1) """
NULL
string(1) "A"

```

**程序 2：**

```php
<?php
// PHP code to illustrate the
// IntlChar::getBidiPairedBracket() function

// Declare an array $arr
$arr = array("G", "{", "^", ")", "6", "{}", "))", "\t");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::getBidiPairedBracket($val));
}
?>
```

**输出：**

```php
string(1) "G"
string(1) "}"
string(1) "^"
string(1) "("
string(1) "6"
NULL
NULL
string(1) "    "

```

**相关文章：**

*   [php|IntlChar：：ToTitle()函数](https://www.geeksforgeeks.org/php-intlchartotitle-function/)
*   [php|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)
*   [php|IntlChar charType()函数](https://www.geeksforgeeks.org/php-intlchar-chartype-function/)

**引用：**[http://php.net/manual/en/intlchar.getbidipairedbracket.php](http://php.net/manual/en/intlchar.getbidipairedbracket.php)
# PHP|IntlChar：：charName()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharcharname-function/](https://www.geeksforgeeks.org/php-intlcharcharname-function/)

**IntlChar：：charName()**函数是 PHP 中的内置函数，用于检索 Unicode 字符的名称。

**语法：**

```
*string* IntlChar::charName( $codepoint [, $nameChoice = 
IntlChar::UNICODE_CHAR_NAME] )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$codepoint：**此参数是一个字符或整数值，编码为 UTF-8 字符串。
*   **$nameChoice：***$nameChoice*参数满足以下任何常量条件之一：
    *   IntlChar：：UNICODE_CHAR_NAME(默认)
    *   IntlChar：：CHAR_NAME_ALIAS
    *   IntlChar：：CHAR_NAME_CHOICE_COUNT
    *   IntlChar：：UNICODE_10_CHAR_NAME
    *   IntlChar：：Extended_Char_

**注意：**生成的字符名称是 Unicode 1.0 版的现代名称，名称包含“不变”字符*A-Z、0-9、“”和‘-’*，并取决于其*$nameChoice*参数。

**返回值：**此函数返回输入数据对应的名称。 如果没有字符名称，则返回空字符串。

下面的程序演示了 PHP 中的**IntlChar：：charName()**函数。
**程序 1：**

```
<?php
// PHP code to illustrate
// IntlChar::charName ()function

// Input astrick symbol of codepoint value 
// with constraint UNICODE_CHAR_NAME 
var_dump(IntlChar::charName("*"));
var_dump(IntlChar::charName("*", IntlChar::UNICODE_CHAR_NAME));

// Input start bracket symbol of codepoint value 
// with constraint UNICODE_10_CHAR_NAME 
var_dump(IntlChar::charName("("));
var_dump(IntlChar::charName("(", IntlChar::UNICODE_10_CHAR_NAME));

// Input ampersand symbol of codepoint value 
// with constraint EXTENDED_CHAR_NAME
var_dump(IntlChar::charName("&"));
var_dump(IntlChar::charName("&", IntlChar::EXTENDED_CHAR_NAME));

// Input ^ symbol of codepoint value 
// with constraint CHAR_NAME_ALIAS
var_dump(IntlChar::charName("^"));
var_dump(IntlChar::charName("^", IntlChar::CHAR_NAME_ALIAS ));

// Input tile symbol of codepoint value 
//and with constraint CHAR_NAME_CHOICE_COUNT
var_dump(IntlChar::charName("`"));
var_dump(IntlChar::charName("`", IntlChar::CHAR_NAME_CHOICE_COUNT));

// Input space of codepoint value
var_dump(IntlChar::charName(" "));

// Input space in codepoint value with 
// UNICODE_CHAR_NAME condition
var_dump(IntlChar::charName(" ", IntlChar::UNICODE_CHAR_NAME));

// Input Alphabet both Capital and Small character
// condition EXTENDED_CHAR_NAME
// and UNICODE_10_CHAR_NAME
var_dump(IntlChar::charName("R"));
var_dump(IntlChar::charName("r"));
var_dump(IntlChar::charName("R", IntlChar::EXTENDED_CHAR_NAME));

// Input int codepoint value
var_dump(IntlChar::charName("10"));
var_dump(IntlChar::charName("7"));

// Input Null codepoint value
var_dump(IntlChar::charName("\u{0000}"));

?>
```

发帖主题：Re：Колибри0.7.0

```
string(8) "ASTERISK" 
string(8) "ASTERISK" 

string(16) "LEFT PARENTHESIS" 
string(0) "" 

string(9) "AMPERSAND" 
string(9) "AMPERSAND" 

string(17) "CIRCUMFLEX ACCENT" 
string(0) "" 

string(12) "GRAVE ACCENT" 
NULL 

string(5) "SPACE" 
string(5) "SPACE" 

string(22) "LATIN CAPITAL LETTER R" 
string(20) "LATIN SMALL LETTER R" 
string(22) "LATIN CAPITAL LETTER R" 

NULL 
string(11) "DIGIT SEVEN" 

string(0) "" 

```

**程序 2：**

```
<?php

// PHP code to illustrate
// IntlChar::charName() function

// Declare an array $arr
$arr = array("G", ".", "8", "/", "000", "\t");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::charName($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```
string(22) "LATIN CAPITAL LETTER G" 
string(9) "FULL STOP" 
string(11) "DIGIT EIGHT" 
string(7) "SOLIDUS" 
NULL 
string(0) "" 

```

**相关文章：**

*   [IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)
*   [IntlChar：：isalpha()函数](https://www.geeksforgeeks.org/php-intlcharisalpha-function/)
*   [IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)

**引用：**[http://php.net/manual/en/intlchar.charname.php](http://php.net/manual/en/intlchar.charname.php)
# PHP|IntlChar：：isJavaSpaceChar()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisjavaspacechar-function/](https://www.geeksforgeeks.org/php-intlcharisjavaspacechar-function/)

**IntlChar：：isJavaSpaceChar()**函数是 PHP 中的一个内置函数，用于根据 Java 检查输入的字符代码点是否为空格字符。 对于不包括控制字符的常规类别为“Z”(分隔符)的字符，其值为 True。
**语法：**和

```
*bool* IntlChar::isJavaSpaceChar( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数*$codepoint*是一个字符或整数值，编码为 UTF-8 字符串。
**返回值：**如果*$codepoint*根据 java 是空格字符，则返回 True，否则返回 False。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：isJavaSpaceChar()**函数

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaSpaceChar()

// Input control character codepoint value
var_dump(IntlChar::isJavaSpaceChar("\n"));

// Input control character codepoint value
var_dump(IntlChar::isJavaSpaceChar("\r"));

// Input string codepoint value with
// Capital and small letter
var_dump(IntlChar::isJavaSpaceChar("V"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isJavaSpaceChar("\u{00A0}"));

// Input symbolic space codepoint value
var_dump(IntlChar::isJavaSpaceChar(" "));

// Input symbolic codepoint value
var_dump(IntlChar::isJavaSpaceChar(" ^ "));

// Input string codepoint value
var_dump(IntlChar::isJavaSpaceChar("Bug"));

// Input int codepoint value
var_dump(IntlChar::isJavaSpaceChar("3 "));

?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(false) 
bool(false) 
bool(false) 
bool(true) 
bool(true) 
NULL 
NULL 
NULL 
```

**程序 2：**和

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaSpaceChar()

// Declare an array with
// different codepoint value
$arr = array("\\",
             " ",
             "\n",
             " #",
             "\t",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isJavaSpaceChar($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(false)
bool(true)
bool(false)
NULL
bool(false)
```

**相关文章：**和

*   [PHP|IntlChar：：isJavaIDPart()函数](https://www.geeksforgeeks.org/php-intlcharisjavaidpart-function/)
*   [PHP|IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)
*   [PHP|IntlChar：：isIDPart()函数](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)

**引用：**[http://php.net/manual/en/intlchar.isjavaspacechar.php](http://php.net/manual/en/intlchar.isjavaspacechar.php)
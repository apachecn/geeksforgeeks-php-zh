# PHP|IntlChar：：isJavaIDStart()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisjavaidstart-function/](https://www.geeksforgeeks.org/php-intlcharisjavaidstart-function/)

**IntlChar：：isJavaIDStart()**函数是 PHP 中的一个内置函数，用于检查输入字符代码点是否允许，因为第一个字符是 Java 标识符。 对于一般类别为“SC”(货币符号)和“Pc”(连接标点符号)的字符为 True。

**语法：**

```
*bool* IntlChar::isJavaIDStart( $codepoint )

```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数*$codepoint*是一个字符或整数值，编码为 UTF-8 字符串。

**返回值：**如果*$codepoint*以 Java 标识符字符开头，则返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isJavaIDStart()**函数：

**程序 1：**

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaIDStart()

// Input string codepoint value with
// Capital and small letter
var_dump(IntlChar::isJavaIDStart("R"));

// Input string codepoint value with small character
var_dump(IntlChar::isJavaIDStart("r"));

// Input control character codepoint value
var_dump(IntlChar::isJavaIDStart("\n"));

// Input string codepoint value
var_dump(IntlChar::isJavaIDStart("Bug"));

// Input int codepoint value
var_dump(IntlChar::isJavaIDStart("3 "));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::isJavaIDStart("\u{007F}"));

// Input symbolic codepoint value
var_dump(IntlChar::isJavaIDStart(" @ "));
var_dump(IntlChar::isJavaIDStart(" $ "));

?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
bool(true)
bool(false)
NULL
NULL
bool(false)
NULL
NULL

```

**程序 2：**

## PHP

```
<?php
// PHP function to illustrate the
// use of IntlChar::isJavaIDStart()

// Declare an array with
// different codepoint value
$arr = array("C",
             " ",
             "\n",
             " #",
             "\t",
             "Code",
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::isJavaIDStart($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
bool(false)
bool(false)
NULL
bool(false)
NULL

```

**相关文章：**

*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)
*   [IntlChar：：isIDPart()函数](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)
*   [IntlChar：：isISOControl()函数](https://www.geeksforgeeks.org/php-intlcharisisocontrol-function/)

**引用：**[http://php.net/manual/en/intlchar.isjavaidstart.php](http://php.net/manual/en/intlchar.isjavaidstart.php)
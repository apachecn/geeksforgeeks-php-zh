# PHP|IntlChar digit()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-digit-function/](https://www.geeksforgeeks.org/php-intlchar-digit-function/)

**IntlChar：：Digit()**函数是 PHP 中的一个内置函数，用于获取给定基数的代码点的十进制位值。 此函数返回以指定基数表示的码位的十进制位值。

**语法：**

```
*int* IntlChar::digit( $codepoint, $radix )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$codepoint：***$codepoint*的值是一个整数或字符，编码为 UTF-8 字符串。
*   **$RADIX：**可选参数。 其默认值为 10。

**返回值：**此函数返回由给定基数中的字符表示的数字，如果没有值或值超过基数，则返回 False。

**注意：**有效和无效的函数参数：

*   如果*$RADIX*或*$digit*都无效，则返回 NULL。
*   如果*$RADIX*参数的值介于$RADIX>=2 和$RADIX<=36 之间，则它是有效的。
*   如果该数字的值为 0<=数字
*   该字符具有十进制数字值。 此字符属于常规类别 ND(十进制数字)和数字类型 DECIMAL。
*   字符是介于‘A’到‘Z’之间的大写拉丁字母。 那么字符值是 c-‘A’+10。
*   字符是‘a’到‘z’之间的小写拉丁字母。 则字符值为 ch-‘a’+10。
*   可识别来自 ASCII 范围(0061..007A、0041.005A)以及全宽 ASCII 范围(FF41..FF5A、FF21..FF3A)的拉丁字母。

下面的程序演示了 PHP 中的**IntlChar：：Digit()**函数：

**程序 1：**

```
<?php

// PHP code to illustrate IntlChar::digit()
// function

// Input data is single digit
var_dump(IntlChar::digit("6"));

// Input data is single digit
var_dump(IntlChar::digit("3"));

// Input data is character type
var_dump(IntlChar::digit("A"));

// // Input data is character type with base
var_dump(IntlChar::digit("P", 16));

// // Input data is character type with base
var_dump(IntlChar::digit("9", 2));
?>
```

**Output:**

```
int(6)
int(3)
bool(false)
bool(false)
bool(false)

```

**程序 2：**

```
<?php
// PHP code to illustrate IntlChar::digit()

// Declare an array $arr
$arr = array("G", "GeeksforGeeks", "^", "1001", "6", "\n",
                                             "\n\n", "\t");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::digit($val));
}
?>
```

**Output:**

```
bool(false)
NULL
bool(false)
NULL
int(6)
bool(false)
NULL
bool(false)

```

**相关文章：**

*   [PHP|IntlChar：：isdigit()函数](https://www.geeksforgeeks.org/php-intlcharisdigit-function/)
*   [PHP|IntlChar：：forDigit()函数](https://www.geeksforgeeks.org/php-intlcharfordigit-function/)
*   [PHP|IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)

**引用：**[http://php.net/manual/en/intlchar.digit.php](http://php.net/manual/en/intlchar.digit.php)
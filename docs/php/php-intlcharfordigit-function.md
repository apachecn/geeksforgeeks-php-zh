# PHP|IntlChar：：forDigit()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharfordigit-function/](https://www.geeksforgeeks.org/php-intlcharfordigit-function/)

**IntlChar：：forDigit()**函数是 PHP 中的一个内置函数，用于确定指定基数中特定数字的字符表示形式。

**语法：**

```
*int* IntlChar::forDigit( $digit, $radix )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$digit:** this is a required parameter. It is the number to be converted to characters.
*   **$RADIX:** optional parameters. Its default value is 10.

**返回值：**返回指定基数中指定数字的字符表示形式。

**注意：**有效和无效的函数参数：

*   如果$RADIX 或$DIGHT 都无效，则返回 NULL。
*   如果 RADIX 参数的值介于$RADIX>=2 和$RADIX<=36 之间，则它是有效的。
*   如果该数字的值为 0<=数字
*   如果是数字：digit<10，则返回‘0’+digit 之和，否则返回‘a’+digit-10。

下面的程序演示了 PHP 中的**IntlChar：：forDigit()**函数：

**程序 1：**

```
<?php
// PHP function to illustrate 
// the use of IntlChar::forDigit()

// Input int codepoint value 
var_dump(IntlChar::forDigit(0));

// Input int codepoint value 
var_dump(IntlChar::forDigit(1));

//Input int codepoint value 
var_dump(IntlChar::forDigit(10));

// Input int codepoint value 
var_dump(IntlChar::forDigit(10, 2018));

// Input float codepoint value 
var_dump(IntlChar::forDigit(20999.1811));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
// PHP function to illustrate the
// use of IntlChar::forDigit()

// Declare an array with
// different codepoint value 
$arr = array("7",
            (50), 
            "8",
            "0",

        );

// For loop condition to check 
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::forDigit($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 3：**下面是函数实现，如果传递参数符号或字符，则会给出错误。

```
<?php
// PHP function to illustrate 
// the use of IntlChar::forDigit()

//Input char codepoint value 
var_dump(IntlChar::forDigit("Geeks"));

//Input char codepoint value 
var_dump(IntlChar::forDigit("X"));

//Input control codepoint value 
var_dump(IntlChar::forDigit("\n"));

//Input symbolic  codepoint value 
var_dump(IntlChar::forDigit("@"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)
*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)

**引用：**[http://php.net/manual/en/intlchar.fordigit.php](http://php.net/manual/en/intlchar.fordigit.php)
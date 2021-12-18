# PHP|IntlChar isfined()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-isdefined-function/](https://www.geeksforgeeks.org/php-intlchar-isdefined-function/)

**IntlChar：：isfined()**函数是 PHP 中的内置函数，用于检查是否定义了代码点。 如果该角色被分配了角色，则该角色被认为是被确定的。 对于 CN(其他，未分配)以外的一般类别为 True。

**语法：**

```
*bool* IntlChar::isdefined ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**如果*$codepoint*是定义的字符，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的**IntlChar：：isfined()**函数：

**程序 1：**

```
<?php

// PHP function to illustrate 
// the use of IntlChar::isdefined()

// Input data is character type
var_dump(IntlChar::isdefined("A"));

// Input data is character type
var_dump(IntlChar::isdefined(" "));

// Input data is unicode character
var_dump(IntlChar::isdefined("\u{FDD0}"));

// Input data is string type
var_dump(IntlChar::isdefined("XYZ"));

// Input data is character type
var_dump(IntlChar::isdefined("5"));

?>
```

**输出：**

```
bool(true)
bool(true)
bool(false)
NULL
bool(true)

```

**程序 2：**

```
<?php
// PHP code to illustrate IntlChar::isdefined()

// Declare an array $arr
$arr = array("G", "GeeksforGeeks", "^", "1001", "6", "\n",
                                             "\n\n", "\t");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::isdefined($val));
}
?>
```

**输出：**

```
bool(true)
NULL
bool(true)
NULL
bool(true)
bool(true)
NULL
bool(true)

```

**相关文章：**

*   [php|IntlChar：：charName()函数](https://www.geeksforgeeks.org/php-intlcharcharname-function/)
*   [php|IntlChar：：issup()函数](https://www.geeksforgeeks.org/php-intlcharisupper-function/)

**引用：**[http://php.net/manual/en/intlchar.isdefined.php](http://php.net/manual/en/intlchar.isdefined.php)
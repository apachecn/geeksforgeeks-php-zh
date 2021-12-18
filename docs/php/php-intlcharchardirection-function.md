# PHP|IntlChar charDirection()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharchardirection-function/](https://www.geeksforgeeks.org/php-intlcharchardirection-function/)

**IntlChar：：charDirection()**函数是 PHP 中的一个内置函数，用于获取代码点的双向类别值。 它返回在 Unicode 双向算法中使用的代码点的双向类别值。

**语法：**

```
*int* IntlChar::charDirection ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**此函数返回双向类别值，如下所示：

*   IntlChar：：CHAR_DIRECTION_LEFT_TO_RIGHT
*   IntlChar：：CHAR_DIRECTION_RIGHT_TO_LEFT
*   IntlChar：：CHAR_DIRECTION_EERIAL_NUMBER
*   IntlChar：：CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR
*   IntlChar：：CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR

*   IntlChar：：Char_Direction_Arial_Number
*   IntlChar：：CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR
*   IntlChar：：CHAR_DIRECTION_BLOCK_SELEATOR
*   IntlChar：：CHAR_DIRECTION_SECTION
*   IntlChar：：CHAR_DIRECTION_WITH_SPACE_NERIAL
*   IntlChar：：CHAR_DIRECTION_OTHER_NERSITAL[.。 _ 右 _ 嵌入
*   IntlChar：：CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE
*   IntlChar：：CHAR_DIRECTION_RIGHT_TO_LEFT_ 阿拉伯语
*   IntlChar：：CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING
*   IntlChar：：CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE
*   IntlChar：：CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT
*   IntlChar：：CHAR_DIRECTION。 _DIR_NON_SPOGING_MARK
*   International character:: CHAR_DIRECTION_BORDURE_NERIAL
*   IntlChar：：CHAR_DIRECTION_FIRST_STRONG_ISOLATE
*   IntlChar：：CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE
*   IntlChar：：CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE
*   IntlChar：：CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE
*   IntlChar：：CHAR_DIRECTION_CHAR_DIRECTION_COUNT

下面的程序演示了 PHP 中的**IntlChar：：charDirection()**函数：

**程序 1：**

```
<?php

// PHP code to illustrate IntlChar::charDirection()
// function

// Input data is character type
var_dump(IntlChar::charDirection("A") === 
           IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT);

// Input data is unicode character
var_dump(IntlChar::charDirection("\u{05E9}") === 
           IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);

// Input data is character type
var_dump(IntlChar::charDirection("+") === 
IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR);

// Input data is character type
var_dump(IntlChar::charDirection(".") === 
  IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR);

// Input data is string type
var_dump(IntlChar::charDirection("ABC") === 
            IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);

// Input data is character type
var_dump(IntlChar::charDirection("c") === 
            IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);

// Input data is character type
var_dump(IntlChar::charDirection("O") === 
            IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT);
?>
```

**输出：**

```
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(true)

```

**程序 2：**

```
<?php

// PHP code to illustrate IntlChar::charDirection()
// function

// Input data is character type
var_dump(IntlChar::charDirection("A"));

// Input data is unicode character
var_dump(IntlChar::charDirection("\u{05E9}"));

// Input data is character type
var_dump(IntlChar::charDirection("+"));

// Input data is character type
var_dump(IntlChar::charDirection("."));

// Input data is string type
var_dump(IntlChar::charDirection("ABC"));

// Input data is character type
var_dump(IntlChar::charDirection("c"));

// Input data is character type
var_dump(IntlChar::charDirection("O"));
?>
```

**输出：**

```
int(0)
int(1)
int(3)
int(6)
NULL
int(0)
int(0)

```

**相关文章：**

*   [php|IntlChar：：islow()函数](https://www.geeksforgeeks.org/php-intlcharislower-function/)
*   [php|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)

**引用：**[http://php.net/manual/en/intlchar.chardirection.php](http://php.net/manual/en/intlchar.chardirection.php)
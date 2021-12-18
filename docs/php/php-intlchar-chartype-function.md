# PHP|IntlChar charType()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-chartype-function/](https://www.geeksforgeeks.org/php-intlchar-chartype-function/)

**IntlChar：：charType()**函数是 PHP 中的一个内置函数，用于获取代码点的一般类别值。 此函数返回代码点的常规类别值。

**语法：**

```php
*int* IntlChar::charType ( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*值是整数值或字符，编码为*UTF-8*字符串。

**返回值：**此函数返回如下所列的一般类别内容：

*   IntlChar：：CHAR_CATEGORY_UNASSIGNED
*   IntlChar：：CHAR_CATEGORY_GROUAL_OTHER_TYPERS
*   IntlChar：：CHAR_CATEGORY_UPERCASE_Letter
*   IntlChar：：CHAR_CATEGORY_LOWERCATY_Letter

*   IntlChar：：CHAR_CATEGORY_OTHER_Letter
*   IntlChar：：Char_Category_Non_Spacing_Mark
*   IntlChar：：CHAR_CATEGORY_ENCLOCING_MARK
*   IntlChar：：CHAR_CATEGORY_COMBINING_SPACING_MARK
*   IntlChar：：CHAR_CATEGORY_DECIMAL_DIGITAL_NUMBER
*   IntlChar.。 ]IntlChar：：CHAR_CATEGORY_OTHER_NUMBER
*   IntlChar：：CHAR_CATEGORY_SPACE_SEARATOR
*   IntlChar：：CHAR_CATEGORY_LINE_SEPARATOR
*   IntlChar：：CHAR_CATEGORY_PARAGE_SEPAGATOR
*   IntlChar：：CHAR_CATEGORY_CONTROL_CHAR
*   IntlChar：：t41]IntlChar：：CHAR_CATEGORY_SURROGATE
*   IntlChar：：CHAR_CATEGORY_DASH_PERTURATION
*   IntlChar：：CHAR_CATEGORY_START_START
*   IntlChar：：CHAR_CATEGORY_END_SPERTURATION
*   IntlChar：：CHAR_CATEGORY_CONNECTOR_PERTURATION

*   IntlChar：：CHAR_CATEGORY_MODIFIER_SYMBOL
*   IntlChar：：CHAR_CATEGORY_OTHER_SYMBOL
*   IntlChar：：CHAR_CATEGORY_INTERIAL_SYMBORY
*   IntlChar：：CHAR_CATEGORY_FINAL_PERTURATION
*   IntlChar：：CHAR_CATEGORY

下面的程序演示了 PHP 中的**IntlChar：：charType()**函数：

**程序 1：**

```php
<?php

// PHP code to illustrate IntlChar::charType()
// function

// Input data is character type
var_dump(IntlChar::charType("A") === 
  IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER);

// Input data is character type
var_dump(IntlChar::charType(".") === 
 IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION);

// Input data is character type
var_dump(IntlChar::charType("\t") === 
      IntlChar::CHAR_CATEGORY_CONTROL_CHAR);

// Input data is unicode character
var_dump(IntlChar::charType("\u{2603}") === 
      IntlChar::CHAR_CATEGORY_OTHER_SYMBOL);

// Input data is string type
var_dump(IntlChar::charType("ABC") === 
 IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION);

// Input data is character type
var_dump(IntlChar::charType("\n") === 
      IntlChar::CHAR_CATEGORY_CONTROL_CHAR);
?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(true)

```

**程序 2：**

```php
<?php

// PHP code to illustrate IntlChar::charType()
// function

// Input data is character type
var_dump(IntlChar::charType("A"));

// Input data is character type
var_dump(IntlChar::charType("."));

// Input data is character type
var_dump(IntlChar::charType("\t"));

// Input data is unicode character
var_dump(IntlChar::charType("\u{2603}"));

// Input data is string type
var_dump(IntlChar::charType("ABC"));

// Input data is character type
var_dump(IntlChar::charType("\n"));
?>
```

**输出：**

```php
int(1)
int(23)
int(15)
int(27)
NULL
int(15)

```

**相关文章：**

*   [php|IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)
*   [php|IntlChar isMirrored()函数](https://www.geeksforgeeks.org/php-intlchar-ismirrored-function/)
*   [php|IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)

**引用：**[http://php.net/manual/en/intlchar.chartype.php](http://php.net/manual/en/intlchar.chartype.php)
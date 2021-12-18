# PHP|IntlChar getPropertyValueEnum()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getpropertyvalueenum-function/](https://www.geeksforgeeks.org/php-intlchar-getpropertyvalueenum-function/)

**IntlChar getPropertyValueEnum()**函数是 PHP 中的一个内置函数，用于从给定值获取属性值。

**语法：**

```php
*int* IntlChar::getPropertyValueEnum( $property, $name )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$property:** it stores IntlChar::Property_* constants.
*   **$name:** it stores the name value to be stored.

**返回值：**如果给定的名称与任何属性都不匹配或该属性无效，则返回相应的值 INTEGER 或 IntlChar：：PROPERTY_INVALID_CODE。

下面的程序演示了 PHP 中的**IntlChar：：getPropertyValueEnum()**函数：

**程序：**

```php
<?php
// PHP program to implement IntlChar::getPropertyValueEnum() function

// Unicode property constant and it corresponding name is same
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS,
        'RIGHT_TO_LEFT') === IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);

// Unicode property constant and it corresponding name is same
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BLOCK,
        'greek') === IntlChar::BLOCK_CODE_GREEK);

// Unicode property constant and it name is corresponding name is same
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS,
        'some made-up string') === IntlChar::PROPERTY_INVALID_CODE);

// Unicode property constant and it name is not matching so it return false
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS,
        'RIGHT_TO_LEFT') === IntlChar::BLOCK_CODE_GREEK);

?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/intlchar.getpropertyvalueenum.php](https://www.php.net/manual/en/intlchar.getpropertyvalueenum.php)
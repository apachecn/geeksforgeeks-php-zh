# PHP|IntlChar getPropertyValueName()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getpropertyvaluename-function/](https://www.geeksforgeeks.org/php-intlchar-getpropertyvaluename-function/)

**IntlChar：：getPropertyValueName()**函数是 PHP 中的内置函数，用于获取属性值的 Unicode 名称。 它将根据 PropertyValueAliases.txt(Unicode 数据库文件)中的数据。

**语法：**

```php
*string* IntlChar::getPropertyValueName( $property, $value, 
$nameChoice = IntlChar::LONG_PROPERTY_NAME )
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **attribute:** it is used for lookup tasks based on the Unicode attribute. It is very similar to the IntlChar::Property_* constant. False is returned if it is out of range or if the method is not compatible with the given value.
*   **value:** it will be a selector for a given attribute. False is returned if it is out of range or if the method is not compatible with the given value. These values will range from 0 to the maximum. In addition, there will be several exceptions. They are:
    *   **IntlChar::Property_Canonical_Comping_CLASS** values are not contiguous at all. In addition, the range will be from 0 to 240.
    *   The **IntlChar::Property_BLOCK** value starts with a non-zero value IntlChar::BLOCK_CODE_BASIC_ Latin.
*   **name selection:** to see which names to get, it will be the selector for that name. False is returned if it is out of range or if the method is not compatible with the given value. In most cases, all values will be long-term values. Some people may have short names, but others will not. For other names, Unicode will allow. If they exist, they are returned by adding 1, 2, 3, and so on to the IntlChar::LONG_PROPERTY_NAME.

**返回值：**如果 nameChoice 或属性完全超出范围，则返回 False。 否则，将返回该名称。 如果将提供 nameChoice，则返回 False。 如果 IntlChar：：SHORT_PROPERTY_NAME 返回 FALSE，则 IntlChar：：LONG_PROPERTY_NAME(及更高版本)仍可能返回非 FALSE 值。

**程序：**

```php
<?php

// PHP program to uses IntlChar::getPropertyValueName()
// function

var_dump(IntlChar::getPropertyValueName
   (IntlChar::PROPERTY_INT_START, IntlChar::BLOCK_CODE_TELUGU));

var_dump(IntlChar::getPropertyValueName
                (IntlChar::PROPERTY_GENERAL_CATEGORY, IntlChar::
     BLOCK_CODE_IPA_EXTENSIONS, IntlChar::SHORT_PROPERTY_NAME));

var_dump(IntlChar::getPropertyValueName
                      (IntlChar::PROPERTY_LINE_BREAK, IntlChar::
            BLOCK_CODE_DINGBATS, IntlChar::LONG_PROPERTY_NAME));

var_dump(IntlChar::getPropertyValueName
                    (IntlChar::PROPERTY_BINARY_LIMIT, IntlChar::
           BLOCK_CODE_BAMUM, IntlChar::LONG_PROPERTY_NAME + 1));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/intlchar.getpropertyvaluename.php](https://www.php.net/manual/en/intlchar.getpropertyvaluename.php)
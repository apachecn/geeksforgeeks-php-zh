# PHP|IntlChar getPropertyEnum()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getpropertyenum-function/](https://www.geeksforgeeks.org/php-intlchar-getpropertyenum-function/)

**IntlChar：：getPropertyEnum()函数**是 PHP 中的一个内置函数，用于获取给定属性名的属性常量值。 属性名称将在 PropertyAliases.txt 中指定，这是一个 Unicode 数据库文件。 所有类型的变体都可以在其中识别，无论是长的、短的还是其他的。 此外，合成名称“General_Category_Mask”(缩写为“GCM”)由函数映射到 IntlChar：：Property_General_CATEGORY_MASK 属性。 还要注意，这里提到的这些名称不会出现在 PropertyAliases.txt 中。 IntlChar：：getPropertyName()函数会对此函数进行补充，反之亦然。

**语法：**

```php
*int* IntlChar::getPropertyEnum( $alias )
```

**参数：**此函数接受单个参数**别名**，该参数的别名是要匹配的属性的名称。 名称的比较是使用“松散匹配”进行的。 这些都在 PropertyAliases.txt 中进行了描述。

**返回值：**如果是常量值，则返回 IntlChar：：Property_Value。 否则，如果给出的名称与任何属性都不匹配，则将返回 IntlChar：：Property_INVALID_CODE。

下面的程序演示了 PHP 中的**IntlChar：：getPropertyEnum()**函数：

**程序：**

```php
<?php

// PHP program to uses IntlChar::getPropertyEnum()
// function

// This function uses IntlChar::PROPERTY_* constants
var_dump(IntlChar::getPropertyEnum('Bidi_Class') === IntlChar
                                    ::PROPERTY_NUMERIC_VALUE);

var_dump(IntlChar::getPropertyEnum('script') === IntlChar
                                    ::PROPERTY_SCRIPT);

var_dump(IntlChar::getPropertyEnum('IDEOGRAPHIC')=== IntlChar
                ::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS);

var_dump(IntlChar::getPropertyEnum('Some made-up string') === 
                            IntlChar::PROPERTY_INVALID_CODE);

var_dump(IntlChar::getPropertyEnum('script') === IntlChar
                                    ::PROPERTY_NUMERIC_TYPE);

?>
```

**输出：**

```php
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/intlchar.getpropertyenum.php](https://www.php.net/manual/en/intlchar.getpropertyenum.php)
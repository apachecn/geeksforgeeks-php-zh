# PHP|IntlChar getIntPropertyMinValue()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getintpropertyminvalue-function/](https://www.geeksforgeeks.org/php-intlchar-getintpropertyminvalue-function/)

IntlChar：：getIntPropertyMinValue()函数是 PHP 中的内置函数，用于获取 Unicode 属性的最小值。 这可以用于访问信息以及操作 Unicode 字符。 对于枚举/整型/二进制 Unicode 属性，这将获得最小值。

**语法：**

```php
*int* IntlChar::getIntPropertyMinValue( $property )
```

**参数：**此函数接受单个参数**$property**，该参数用于基于 Unicode 属性的查找任务。 它非常类似于 IntlChar：：Property_*常量。

**返回值：**对于 Unicode 属性，它是 IntlChar：：getIntPropertyValue()函数要返回的最大值。 如果属性的选择器大大超出范围，则返回 0。

下面的程序演示了 PHP 中的 IntlChar：：getIntPropertyMinValue()函数：

**程序：**

```php
<?php

// PHP program to uses IntlChar::getIntPropertyMinValue()
// function

// This function uses IntlChar::PROPERTY_* constants
var_dump(IntlChar::getIntPropertyMinValue
                    (IntlChar::CHAR_CATEGORY_ENCLOSING_MARK));

var_dump(IntlChar::getIntPropertyMinValue
                            (IntlChar::BLOCK_CODE_BENGALI));

var_dump(IntlChar::getIntPropertyMinValue
                (IntlChar::PROPERTY_GRAPHEME_CLUSTER_BREAK));

var_dump(IntlChar::getIntPropertyMinValue
                    (IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL));

var_dump(IntlChar::getIntPropertyMinValue
                                        (IntlChar::NT_DIGIT));

var_dump(IntlChar::getIntPropertyMinValue
                (IntlChar::LB_CONDITIONAL_JAPANESE_STARTER));

var_dump(IntlChar::getIntPropertyMinValue(49)); 

?>
```

**输出：**

```php
int(0)
int(0)
int(0)
int(0)
int(0)
int(0)
int(0)

```

**引用：**[https://www.php.net/manual/en/intlchar.getintpropertyminvalue.php](https://www.php.net/manual/en/intlchar.getintpropertyminvalue.php)
# PHP|IntlChar getIntPropertyMaxValue()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getintpropertymaxvalue-function/](https://www.geeksforgeeks.org/php-intlchar-getintpropertymaxvalue-function/)

**IntlChar：：getIntPropertyMaxValue()**函数是 PHP 中的内置函数，用于获取 Unicode 属性的最大值。 这可以用于访问信息以及操作 Unicode 字符。 对于枚举/整型/二进制 Unicode 属性，这将获得最大值。

**语法：**

```
*int* IntlChar::getIntPropertyMaxValue( $property ) 

```

**参数：**此函数接受单个参数**$property**，该参数用于基于 Unicode 属性的查找任务。 它非常类似于 IntlChar：：Property_*常量。

**返回值：**对于 Unicode 属性，它是 IntlChar：：getIntPropertyValue()函数要返回的最大值。 如果<=0，则此属性的选择器被视为超出范围。

下面的程序演示了 PHP 中的*IntlChar：：getIntPropertyMaxValue()*函数：

**程序：**

```
<?php

// PHP program to uses IntlChar::getIntPropertyMaxValue()
// function

// This function uses IntlChar::PROPERTY_* constants
var_dump(IntlChar::getIntPropertyMaxValue
                    (IntlChar::CHAR_CATEGORY_ENCLOSING_MARK));
var_dump(IntlChar::getIntPropertyMaxValue
                              (IntlChar::BLOCK_CODE_BENGALI));
var_dump(IntlChar::getIntPropertyMaxValue
                 (IntlChar::PROPERTY_GRAPHEME_CLUSTER_BREAK));
var_dump(IntlChar::getIntPropertyMaxValue
                   (IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL));
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::NT_DIGIT));

var_dump(IntlChar::getIntPropertyMaxValue
                  (IntlChar::LB_CONDITIONAL_JAPANESE_STARTER));
var_dump(IntlChar::getIntPropertyMaxValue(69)); 

?>
```

发帖主题：Re：Колибри0.7.0

```
int(1)
int(1)
int(12)
int(1)
int(1)
int(1)
int(-1)

```

**引用：**
[https://www.php.net/manual/en/intlchar.getintpropertymaxvalue.php](https://www.php.net/manual/en/intlchar.getintpropertymaxvalue.php)
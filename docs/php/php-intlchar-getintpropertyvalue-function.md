# PHP|IntlChar getIntPropertyValue()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getintpropertyvalue-function/](https://www.geeksforgeeks.org/php-intlchar-getintpropertyvalue-function/)

**IntlChar：：getIntPropertyValue()**函数是 PHP 中的内置函数，用于获取代码点的 Unicode 属性值。
**语法：**和

```
*int* IntlChar::getIntPropertyValue( $codepoint, $property )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$codepoint：**输入参数$codepoint 是一个字符或整数值，编码为*UTF-8*字符串。
*   **$Property**它存储 Unicode 字符常量。 示例：IntlChar：：Property_*常量。

**返回值：**和

*   它返回的数值直接是属性值，或者枚举属性对应于相应属性值枚举类型的枚举常量的数值。
*   它返回二进制 Unicode 属性的布尔值(0/1 或 false/true)。
*   它返回掩码属性的位掩码值。
*   如果属性超出界限，或者 Unicode 版本根本没有该属性的数据，或者没有该代码点的数据，则返回 0。

下面的程序说明 PHP：
**程序 1：**和
中的**IntlChar：：getIntPropertyValue()**函数

## PHP

```
<?php

// Input data is alphabet character type
var_dump(IntlChar::getIntPropertyValue("A",
        IntlChar::PROPERTY_ALPHABETIC) === 1);

// Input data is mirrored brackets character type
var_dump(IntlChar::getIntPropertyValue("[",
        IntlChar::PROPERTY_BIDI_MIRRORED) === 1);

// Input data is Space character type
var_dump(IntlChar::getIntPropertyValue(" ",
        IntlChar::PROPERTY_POSIX_BLANK) === 1);

// Input data is special character type
var_dump(IntlChar::getIntPropertyValue("?",
    IntlChar::PROPERTY_BLOCK) === IntlChar::BLOCK_CODE_GREEK);

?>
```

**Output:** 

```
bool(true)
bool(true)
bool(true)
bool(false)
```
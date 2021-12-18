# PHP|IntlChar hasBinaryProperty()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-hasbinaryproperty-function/](https://www.geeksforgeeks.org/php-intlchar-hasbinaryproperty-function/)

**IntlChar：：hasBinaryProperty()**函数是 PHP 中的内置函数，用于检查代码点的二进制 Unicode 属性。

**语法：**

```
*bool* IntlChar::hasBinaryProperty( $codepoint, $property )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$codepoint:** $codepoint value is an integer value or character, encoded as a UTF-8 string.
*   **$Property:** this stores the IntlChar::Property_* constant.

**返回值：**此函数根据二进制 Unicode 属性返回布尔值(TRUE 或 FALSE)。

下面的程序演示了 PHP 中的**IntlChar：：hasBinaryProperty()**函数：

**程序 1：**

```
<?php

// PHP function to illustrate the use of 
// IntlChar::hasBinaryProperty() function

// Input data is character type 
var_dump(IntlChar::hasBinaryProperty("G", IntlChar::PROPERTY_ALPHABETIC));

// Input data is string type 
var_dump(IntlChar::hasBinaryProperty("Geeks", IntlChar::PROPERTY_ALPHABETIC));

// Input data is mirrored bracket character type 
var_dump(IntlChar::hasBinaryProperty("}", IntlChar::PROPERTY_BIDI_MIRRORED));

// Input data is character type 
var_dump(IntlChar::hasBinaryProperty("%", IntlChar::PROPERTY_BIDI_MIRRORED));
?>
```

**输出：**

```
bool(true)
NULL
bool(true)
bool(false)

```

**程序 2：**

```
<?php

// PHP function to illustrate the use of 
// IntlChar::hasBinaryProperty() function

// Declare an array $arr 
$arr = array("A", "{", "^", ")", "6", "Geeks", "))");

// Loop run for every array element 
foreach ($arr as $val){ 

    // Check each element as code point data 
    var_dump(IntlChar::hasBinaryProperty($val,
                   IntlChar::PROPERTY_BIDI_MIRRORED)); 
} 

?>
```

**输出：**

```
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)
NULL
NULL

```

**引用：**[https://www.php.net/manual/en/intlchar.hasbinaryproperty.php](https://www.php.net/manual/en/intlchar.hasbinaryproperty.php)
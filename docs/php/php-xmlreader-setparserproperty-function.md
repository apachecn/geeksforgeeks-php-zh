# PHP|XMLReader setParserProperty()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-setparserproperty-function/](https://www.geeksforgeeks.org/php-xmlreader-setparserproperty-function/)

**XMLReader：：setParserProperty()函数**是 PHP 中的内置函数，用于设置解析器选项。 此功能可用于对单据进行验证。
**语法：**和

```
*bool* XMLReader::setParserProperty( *int* $property, *bool* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Property：**它指定一个整数，对应于下面给出的解析器选项常量之一：
    *   ***XMLReader：：LOADDTD(1)***这将加载 DTD，但不会进行验证。
    *   ***XMLReader：：DEFAULTATTRS(2)***这将加载 DTD 和默认属性，但不会进行验证。
    *   ***XMLReader：：VALIDATE(3)***这将在解析时加载 DTD 并进行验证。
    *   ***XMLReader：：SUBST_ENTITIES(4)***这将替换实体并展开引用。
*   **$value：**它指定是启用还是禁用该属性。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。
以下示例说明 PHP：
**中的**XMLReader：：setParserProperty()函数**示例 1：**和

*   **data.xml**和

## 超文本标记语言

```
<?xml version="1.0" encoding="utf-8"?>
<div>
    <h1> Sample XML </h1>
</div>
```

*   **index.php**和

## PHP

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file with sample XML
$XMLReader->open('data.xml');

// Set the Parser Property
$XMLReader->setParserProperty(XMLReader::VALIDATE, true);

// Check if XMLReader::VALIDATE is set or not
$isProperty = $XMLReader->getParserProperty(XMLReader::VALIDATE);

if ($isProperty) {
    echo 'Property is set.';
}
?>
```
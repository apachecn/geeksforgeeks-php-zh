# PHP|XMLWriter endAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-endattribute-function/](https://www.geeksforgeeks.org/php-xmlwriter-endattribute-function/)

**XMLWriter：：endAttribute()函数**是 PHP 中的一个内置函数，用于结束使用**XMLWriter：：startAttribute()**函数启动的属性。

**语法：**

```
*bool* XMLWriter::endAttribute( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：endAttribute()函数**：

**示例 1：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start a element
$writer->startElement('div');

// Start the attribute
$writer->startAttribute('attrib');

// Add value to the attribute
$writer->text('value');

// End the attribute
$writer->endAttribute();

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

**输出：**
![](img/942bf6acd49eab7d89c29742d99d57d6.png)

**示例 2：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start a h1 element
$writer->startElement('h1');

// Start the style attribute
$writer->startAttribute('style');

// Add value to the attribute
$writer->text('color:green');

// End the attribute
$writer->endAttribute();

// Add value to the element
$writer->text('GeeksforGeeks');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

**输出：**
![](img/4a637d6ed46f340d1f91a4d5a07827c2.png)

**引用：**[https://www.php.net/manual/en/function.xmlwriter-end-attribute.php](https://www.php.net/manual/en/function.xmlwriter-end-attribute.php)
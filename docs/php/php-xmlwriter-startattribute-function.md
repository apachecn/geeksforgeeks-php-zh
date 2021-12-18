# PHP|XMLWriter startAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-startattribute-function/](https://www.geeksforgeeks.org/php-xmlwriter-startattribute-function/)

**XMLWriter：：startAttribute()函数**是 PHP 中的一个内置函数，用于启动属性。 稍后可以使用 XMLWriter：：endAttribute()函数关闭该属性。

**语法：**

```php
*bool* XMLWriter::startAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：startAttribute()函数**：

**示例 1：**

```php
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

发帖主题：Re：Колибри0.7.0

```php
<?xml version="1.0" encoding="UTF-8"?>
<div attrib="value"/>
```

**示例 2：**在此示例中，我们将向元素添加样式

```php
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
![](img/a482c36aaf072bac6a06caab5a699d37.png)

**引用：**[https://www.php.net/manual/en/function.xmlwriter-start-attribute.php](https://www.php.net/manual/en/function.xmlwriter-start-attribute.php)
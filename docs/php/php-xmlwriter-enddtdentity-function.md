# PHP|XMLWriter endDtdEntity()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-enddtdentity-function/](https://www.geeksforgeeks.org/php-xmlwriter-enddtdentity-function/)

**XMLWriter：：endDtdEntity()函数**是 PHP 中的一个内置函数，用于结束当前的 DTD 实体。 DTD 是 Document Type Definition 的缩写，它定义了 XML 文档的结构、合法元素和属性。 DTD 在网页上不可见，因为它们的行为类似于注释。 实体用于定义特殊字符的快捷方式。

**语法：**

```
*bool* XMLWriter::endDtdEntity( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：endDtdEntity()函数**：

**示例 1：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start the Dtd Entity
$writer->startDtdEntity('entity', true);

// End the Dtd Entity
$writer->endDtdEntity();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.0

```
<?xml version="1.0" encoding="UTF-8"?>
<!ENTITY % entity>
```

**示例 2：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start the Dtd Entity which is
// not going to be visible
$writer->startDtdEntity('entity', true);

// End the Dtd Entity
$writer->endDtdEntity();

// Start a h1 element
$writer->startElement('h1');

// Add a style attribute
$writer->writeAttribute('style', 
          'color:blue;font-size:100;');

// Add text to the element
$writer->text('GeeksforGeeks');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

**输出：**
![](img/6366ef66ef6468b086bf664e177d9b74.png)

**引用：**[https://www.php.net/manual/en/function.xmlwriter-end-dtd-entity.php](https://www.php.net/manual/en/function.xmlwriter-end-dtd-entity.php)
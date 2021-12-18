# PHP|XMLWriter endDocument()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-enddocument-function/](https://www.geeksforgeeks.org/php-xmlwriter-enddocument-function/)

**XMLWriter：：endDocument()函数**是 PHP 中的一个内置函数，用于结束当前文档。

**语法：**

```
*bool* XMLWriter::endDocument( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：endDocument()函数**：

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

// Add value to the element
$writer->text('GeeksforGeeks');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.0

```
<?xml version="1.0" encoding="UTF-8"?>
<div>GeeksforGeeks</div>
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

// Start a h1 element
$writer->startElement('h1');

// Start the style attribute
$writer->startAttribute('style');

// Add value to the attribute
$writer->text('color:green;font-size:80px;');

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

发帖主题：Re：Колибри0.7.0

```
<?xml version="1.0" encoding="UTF-8"?>
<h1 style="color:green;font-size:80px;">GeeksforGeeks</h1>
```

![](img/da052aae1316861e2fee5d404a27088a.png)

**引用：**[https://www.php.net/manual/en/function.xmlwriter-end-document.php](https://www.php.net/manual/en/function.xmlwriter-end-document.php)
# PHP|XMLWriter startDocument()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-startdocument-function/](https://www.geeksforgeeks.org/php-xmlwriter-startdocument-function/)

**XMLWriter：：startDocument()函数**是 PHP 中的一个内置函数，用于启动文档。 然后，本文档需要以*XMLWriter：：endDocument*函数结束。

**语法：**

```php
*bool* XMLWriter::startDocument( *string* $version, 
*string* $encoding, *string* $standalone )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$version(可选)：**它指定文档的版本号，作为 XML 声明的一部分。
*   **$Coding(可选)：**它将文档的编码指定为 XML 声明的一部分。
*   **$STANDALE(可选)：**它指定文档是否为独立文档。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：startDocument()函数**：

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

// Add value to the element
$writer->text('GeeksforGeeks');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.0

```php
<?xml version="1.0" encoding="UTF-8"?>
<div>GeeksforGeeks</div>

```

**示例 2：**

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
$writer->text('color:orange;font-size:80px;');

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
![](img/d5a075ca04a739945a3fd4ab25c9ecfc.png)

**引用：**[https://www.php.net/manual/en/function.xmlwriter-start-document.php](https://www.php.net/manual/en/function.xmlwriter-start-document.php)
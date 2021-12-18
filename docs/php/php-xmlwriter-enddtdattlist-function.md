# PHP|XMLWriter endDtdAttlist()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-enddtdattlist-function/](https://www.geeksforgeeks.org/php-xmlwriter-enddtdattlist-function/)

**XMLWriter：：endDtdAttlist()函数**是 PHP 中的内置函数，用于结束当前的 DTD AttList。 DTD 是 Document Type Definition 的缩写，它定义了 XML 文档的结构、合法元素和属性。 DTD 在网页中不可见，因为它们的行为类似于注释。 在 DTD 中，属性是用 ATTLIST 声明声明的。

**语法：**

```php
*bool* XMLWriter::endDtdAttlist( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：endDtdAttlist()函数**：

**示例 1：**

```php
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start the Dtd Attlist
$writer->startDtdAttlist('geeksforgeeks');

// End the Dtd Attlist
$writer->endDtdAttlist();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start the Dtd Attlist
$writer->startDtdAttlist('This_is_not_visible_in_webpage');

// End the Dtd Attlist
$writer->endDtdAttlist();

// Add text to document
$writer->text('geeksforgeeks');

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.xmlwriter-end-dtd-attlist.php](https://www.php.net/manual/en/function.xmlwriter-end-dtd-attlist.php)
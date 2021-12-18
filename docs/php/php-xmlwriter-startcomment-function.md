# PHP|XMLWriter startComment()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-startcomment-function/](https://www.geeksforgeeks.org/php-xmlwriter-startcomment-function/)

**XMLWriter：：startComment()函数**是 PHP 中的一个内置函数，用于启动注释。 稍后需要使用*XMLWriter：：endComment()*函数关闭此注释。

**语法：**

```php
*bool* XMLWriter::startComment( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：startComment()函数**：

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

// Start a comment
$writer->startComment();

// Add text to the comment
$writer->text('This is a comment');

// End the comment
$writer->endComment();

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

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

// Start a comment
$writer->startComment();

// Add text to the comment which will not be visible
$writer->text('This will not be visible.');

// End the comment
$writer->endComment();

// Add value to the element
$writer->text('This is the visible text.');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.xmlwriter-start-comment.php](https://www.php.net/manual/en/function.xmlwriter-start-comment.php)
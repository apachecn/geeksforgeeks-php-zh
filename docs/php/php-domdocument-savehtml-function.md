# PHP|DOMDocument saveHTML()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-savehtml-function/](https://www.geeksforgeeks.org/php-domdocument-savehtml-function/)

**DOMDocument：：saveHTML()函数**是 PHP 中的一个内置函数，用于从 DOM 表示创建 HTML 文档。 此函数在从头构建 DOM 文档后使用。

**语法：**

```php
*string* DOMDocument::saveHTML( *DOMNode* $node = NULL )
```

**参数：**此函数接受单个参数**$node**，该参数是可选的，用于输出文档的子集。

**返回值：**此函数成功时返回 HTML 文档，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：saveHTML()函数：

**程序：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0');

// Create a root element
$root = $domDocument->createElement('html');

// Append the element to the document as root element
$root = $domDocument->appendChild($root);

// Create a head element
$head = $domDocument->createElement('head');

// Append the element to the document
// as child element
$head = $root->appendChild($head);

// Create a title element
$title = $domDocument->createElement('title');

// Append the element to the document
// as child element
$title = $head->appendChild($title);

// Create a text node
$text = $domDocument->createTextNode(
        'DOMDocument::saveHTML() function');

// Add the text node the the title element
$text = $title->appendChild($text);

// Create a body element
$body = $domDocument->createElement('body');

// Append the element to the document
// as child element
$body = $root->appendChild($body);

// Create a heading element
$h1 = $domDocument->createElement('h1');

// Append the element to the document
$h1 = $body->appendChild($h1);

// Create a text node
$text = $domDocument->createTextNode('GeeksforGeeks');

// Add the text node to the heading element
$text = $h1->appendChild($text);

// Create a heading element
$h2 = $domDocument->createElement('h2');

// Append the element to the document
$h2 = $body->appendChild($h2);

// Create a text node
$text = $domDocument->createTextNode(
            'DOMDocument::saveHTML() function');

// Add the text node to the heading element
$text = $h2->appendChild($text);

// Use saveHTML() function to create
// an HTML document
echo $domDocument->saveHTML();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.savehtml.php](https://www.php.net/manual/en/domdocument.savehtml.php)
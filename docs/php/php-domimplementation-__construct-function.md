# PHP|DOMImplementation__Construction()函数

> Original: [https://www.geeksforgeeks.org/php-domimplementation-__construct-function/](https://www.geeksforgeeks.org/php-domimplementation-__construct-function/)

**DOMImplementation：：__Construct()函数**是 PHP 中的内置函数，用于创建新的 DOMImplementation 对象。

**语法：**

```
 DOMImplementation::__construct( *void* )
```

**参数：**此函数不接受任何参数。

以下示例说明 PHP 中的**DOMImplementation：：__Construct()函数**：

**示例 1：**

```
<?php

// Create a DOMImplementation instance
$documentImplementation = new DOMImplementation();

// Create a document
$document = $documentImplementation->createDocument(null, 'html');

// Get the document element
$html = $document->documentElement;

// Create few element
$heading = $document->createElement('h1');
$text = $document->createTextNode('GeeksforGeeks');

// Append the children
$heading->appendChild($text);
$html->appendChild($heading);

// Render the XML
echo $document->saveXML();
?>
```

**输出：**
![](img/260dd1f2d3da9d8b51ca01d3f1b0f855.png)
**示例 2：**

```
<?php
// Create a DOMImplementation instance
$documentImplementation = new DOMImplementation();

// Create a document
$document = $documentImplementation->createDocument(null, 'html');

// Get the document element
$html = $document->documentElement;

// Create few element
$head = $document->createElement('head');
$title = $document->createElement('title');
$text = $document->createTextNode('GeeksforGeeks');
$body = $document->createElement('body');

// Append the children
$title->appendChild($text);
$head->appendChild($title);
$html->appendChild($head);
$html->appendChild($body);

// Render the XML
echo $document->saveXML();
?>
```

**输出：**
![](img/ce755a8c55445d663e09fdea896c40dd.png)
**参考：**[https://www.php.net/manual/en/domimplementation.construct.php](https://www.php.net/manual/en/domimplementation.construct.php)
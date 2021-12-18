# PHP|DOMImplementation createDocument()函数

> Original: [https://www.geeksforgeeks.org/php-domimplementation-createdocument-function/](https://www.geeksforgeeks.org/php-domimplementation-createdocument-function/)

**DOMImplementation：：createDocument()函数**是 PHP 中的一个内置函数，用于创建带有文档元素的指定类型的 DOMDocument 对象。

**语法：**

```php
*DOMDocument* DOMImplementation::createDocument( *string* $namespaceURI = NULL, 
*string* $qualifiedName = NULL, *DOMDocumentType* $doctype = NULL )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$nampaceURI(可选)：**它指定要创建的文档元素的命名空间 URI。
*   **$qualfiedName(可选)：**它指定要创建的文档元素的限定名称。
*   **$doctype(可选)：**它指定要创建的文档类型或为空。

**返回值：**此函数成功时返回 DOMDocument 对象。

**异常：**此函数抛出**DOM_WRONG_DOCUMENT_ERR**(如果 doctype 已用于不同的文档或从不同的实现创建)或**DOM_NAMESPACE_ERR**(如果命名空间有错误，由**$NAMESPACEURI**和**$QualifiedName**确定)。

以下示例说明 PHP 中的**DOMImplementation：：createDocument()函数**：

**示例 1：**

```php
<?php

// Create a DOMImplementation instance
$documentImplementation = new DOMImplementation();

// Create a document
$document = $documentImplementation->createDocument(null, 'html');

// Get the document element
$html = $document->documentElement;

// Create a HTML element
$head = $document->createElement('html');

// Create a strong element
$title = $document->createElement('strong');
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
![](img/260dd1f2d3da9d8b51ca01d3f1b0f855.png)
**示例 2：**

```php
<?php

// Create a DOMImplementation instance
$documentImplementation = new DOMImplementation();

// Create a document
$document = $documentImplementation->createDocument(null, 'html');

// Get the document element
$html = $document->documentElement;

// Create a HTML element
$head = $document->createElement('html');

// Create a paragraph element
$p = $document->createElement('p');

// Create a text node
$text = $document->createTextNode('GeeksforGeeks');

// Append the children
$p->appendChild($text);

// Set the CSS using attribute 
$p->setAttribute('style', 'color:blue;font-size:100px');

// Append paragraph to the head of document
$head->appendChild($p);

// Append head to the html
$html->appendChild($head);

// Render the XML
echo $document->saveXML();
?>
```

**输出：**
![](img/d8c1146e792848bf70ef04514d69f8f6.png)

**引用：**[https://www.php.net/manual/en/domimplementation.createdocument.php](https://www.php.net/manual/en/domimplementation.createdocument.php)
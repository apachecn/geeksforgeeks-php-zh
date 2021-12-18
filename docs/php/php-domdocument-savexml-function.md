# PHP|DOMDocument saveXML()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-savexml-function/](https://www.geeksforgeeks.org/php-domdocument-savexml-function/)

**DOMDocument：：saveXML()函数**是 PHP 中的一个内置函数，用于从 DOM 表示创建 XML 文档。 此函数是在从头开始构建新的 dom 文档后使用的。

**语法：**

```
*string* DOMDocument::saveXML( *DOMNode* $node, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$node:** this parameter is used only for the output of specific nodes that have no XML declaration, not for the entire document.
*   **$Options:** this parameter adds additional options. Currently, this parameter only supports LIBXML_NOEMPTYTAG.

**返回值：**此函数成功时返回 XML 文档，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：saveXML()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createTextNode() function to create a text node
$domTN = $domDocument->createTextNode('GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domTN);

// Use saveXML() function to save the XML document
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
GeeksforGeeks

```

**程序 2：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createElement() function to create an element node
$domElement = $domDocument->createElement('organization',
                                       'GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domElement);

// Use saveXML() function to create a XML document
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<organization>GeeksforGeeks</organization>

```

**引用：**[https://www.php.net/manual/en/domdocument.savexml.php](https://www.php.net/manual/en/domdocument.savexml.php)
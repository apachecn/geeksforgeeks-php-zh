# PHP|DOMDocument createElementNS()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createelementns-function/](https://www.geeksforgeeks.org/php-domdocument-createelementns-function/)

**DOMDocument：：createElementNS()函数**是 PHP 中的内置函数，用于创建具有关联名称空间的新元素节点。

**语法：**

```
*DOMElement* DOMDocument::createElementNS( *string* $namespaceURI, 
                             *string* $qualifiedName, *string* $value )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$nampaceURI:** this parameter holds the URI of the namespace.
*   **$QualifiedName:** this parameter holds the qualified name of the element, such as the prefix: tag name.
*   **$value:** this parameter holds the value of the element. The default value for this parameter is empty or none, indicating that an empty element has been created.

**返回值：**此函数成功时返回新的 DOMElement，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createElementNS()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument('1.0', 'utf-8');

// Use createElementNS() function to create new
// element node with an associated namespace
$element = $dom->createElementNS('https://www.geeksforgeeks.org/php',
        'php:function', 'Welcome to GeeksforGeeks');

// Append the child element
$dom->appendChild($element);

// Create XML document and diplsy it
echo $dom->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="utf-8"?>
<php:function xmlns:php="https://www.geeksforgeeks.org/php">
    Welcome to GeeksforGeeks
</php:function>

```

**程序 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument('1.0', 'utf-8');

// Use createElementNS() function to create new
// element node with an associated namespace
$element1 = $dom->createElementNS('https://www.geeksforgeeks.org/php',
        'organization:GeeksforGeeks', 'A computer science portal');

$element2 = $dom->createElementNS('https://www.geeks.org/html',
        'php:link', 'Welcome to GeeksforGeeks');

$element3 = $dom->createElementNS('https://www.geeksforgeeks.org/algo',
        'algo:link', 'Best coding platform');

// Append the child element
$dom->appendChild($element1);
$dom->appendChild($element2);
$dom->appendChild($element3);

// Create XML document and diplsy it
echo $dom->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="utf-8"?>
<organization:GeeksforGeeks xmlns:organization
        ="https://www.geeksforgeeks.org/php">
    A computer science portal
</organization:GeeksforGeeks>

<php:link xmlns:php="https://www.geeks.org/html">
    Welcome to GeeksforGeeks
</php:link>

<algo:link xmlns:algo="https://www.geeksforgeeks.org/algo">
    Best coding platform
</algo:link>

```

**引用：**[https://www.php.net/manual/en/domdocument.createelementns.php](https://www.php.net/manual/en/domdocument.createelementns.php)
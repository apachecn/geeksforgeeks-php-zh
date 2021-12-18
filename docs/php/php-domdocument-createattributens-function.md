# PHP|DOMDocument createAttributeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createattributens-function/](https://www.geeksforgeeks.org/php-domdocument-createattributens-function/)

**DOMDocument：：createAttributeNS()函数**是 PHP 中的内置函数，用于创建具有关联名称空间的新属性节点。

**语法：**

```php
*DOMAttr* DOMDocument::createAttributeNS( *string* $namespaceURI, *string* $qualifiedName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI:** this parameter holds the URI of the namespace.
*   **$QualifiedName** this parameter holds the tag name and prefix of the attribute. For example: prefix: tag name.

**返回值：**此函数成功时返回新的 DOMAttr 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createAttributeNS()函数：

**程序：**

```php
<?php

// Store the XML document to the source
$source = <<<XML
<?xml version="1.0" encoding="UTF-8"?>
<root><contact><email>abc@geeksforgeeks.org</email>
<mobile>+91-987654321</mobile></contact></root>
XML;

// Create a new document
$domDocument = new DOMDocument( '1.0' );

// Load the XML file
$domDocument->loadXML( $source );

// Use createAttributeNS() function to create new attribute
// node with an associated namespace
$attrNS = $domDocument->createAttributeNS(
                '{namespace}', 'info:cont_info' );

// Create XML document and display it
echo $domDocument->saveXML() . "\n";

// Assign value to the createAttributeNS
$attrNS->value = 'https://www.geeksforgeeks.org/about/contact-us/';

$domDocument->getElementsByTagName( 'contact' )
            ->item(0)->appendChild( $attrNS );

// Create XML document and display it
print $domDocument->saveXML() . "\n";

?>
```

**输出：**

```php
<?xml version="1.0" encoding="UTF-8"?>
<root xmlns:info="{namespace}">
    <contact>
        <email>abc@geeksforgeeks.org</email>
        <mobile>+91-987654321</mobile>
    </contact>
</root>

<?xml version="1.0" encoding="UTF-8"?>
<root xmlns:info="{namespace}">
    <contact info:cont_info=
        "https://www.geeksforgeeks.org/about/contact-us/">
        <email>abc@geeksforgeeks.org</email>
        <mobile>+91-987654321</mobile>
    </contact>
</root>

```

**引用：**[https://www.php.net/manual/en/domdocument.createattributens.php](https://www.php.net/manual/en/domdocument.createattributens.php)
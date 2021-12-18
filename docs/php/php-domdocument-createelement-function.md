# PHP|DOMDocument createElement()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createelement-function/](https://www.geeksforgeeks.org/php-domdocument-createelement-function/)

**DOMDocument：：createElement()函数**是 PHP 中的内置函数，用于创建 DOMElement 类的新实例。

**语法：**

```
*DOMElement* DOMDocument::createElement( *string* $name, *string* $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name:** this parameter holds the tag name of the element.
*   **$value:** this parameter holds the value of the element. The default value of this function creates an empty element. You can use DOMElement::$nodeValue to set the value of the element later.

**返回值：**此函数成功时返回 DOMElement 类的新实例，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createElement()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createElement() function to add a new element node
$domElement = $domDocument->createElement('organization', 'GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domElement);

// Save XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<organization>GeeksforGeeks</organization>

```

**程序 2：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createElement() function to add a new element node
$domElement1 = $domDocument->createElement('organization');
$domElement2 = $domDocument->createElement('name', 'GeeksforGeeks');
$domElement3 = $domDocument->createElement('address', 'Noida');
$domElement4 = $domDocument->createElement('email', 'abc@geeksforgeeks.org');

// Append element to the document
$domDocument->appendChild($domElement1);
$domElement1->appendChild($domElement2);
$domElement1->appendChild($domElement3);
$domElement1->appendChild($domElement4);

// Save XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<organization>
    <name>GeeksforGeeks</name>
    <address>Noida</address>
    <email>abc@geeksforgeeks.org</email>
</organization>

```

**引用：**[https://www.php.net/manual/en/domdocument.createelement.php](https://www.php.net/manual/en/domdocument.createelement.php)
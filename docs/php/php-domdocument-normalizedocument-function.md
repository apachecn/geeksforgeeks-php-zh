# PHP|DOMDocument NormizeDocument()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-normalizedocument-function/](https://www.geeksforgeeks.org/php-domdocument-normalizedocument-function/)

**DOMDocument：：NormizeDocument()函数**是 PHP 中的一个内置函数，用于规范化文档。 如果您保存并加载了文档，则此函数用于将文档转换为标准格式。

**语法：**

```
*void* DOMDocument::normalizeDocument( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 DOMDocument：：NormizeDocument()函数：

**程序 1：**

```
<?php

// Create a new document
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Create an element
$domElement = $domDocument->createElement('organization', 'GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domElement);

// Use normalizeDocument() function
// to normalize the document
$domDocument->normalizeDocument();

// Create the XML file and display it
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

// Create a new document
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Create an element
$domElement1 = $domDocument->createElement('organization');
$domElement2 = $domDocument->createElement('name', 'GeeksforGeeks');
$domElement3 = $domDocument->createElement('address', 'Noida');
$domElement4 = $domDocument->createElement('email', 'abc@geeksforgeeks.org');

// Append element to the document
$domDocument->appendChild($domElement1);
$domElement1->appendChild($domElement2);
$domElement1->appendChild($domElement3);
$domElement1->appendChild($domElement4);

// Use normalizeDocument() function
// to normalize the document 
$domDocument->normalizeDocument();

// Create the XML file and display it
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

**引用：**[https://www.php.net/manual/en/domdocument.normalizedocument.php](https://www.php.net/manual/en/domdocument.normalizedocument.php)
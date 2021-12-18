# PHP|DOMDocument createComment()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createcomment-function/](https://www.geeksforgeeks.org/php-domdocument-createcomment-function/)

**DOMDocument：：createComment()函数**是 PHP 中的内置函数，用于创建 createComment 类的新实例。

**语法：**

```
*DOMComment* DOMDocument::createComment( *string* $data )
```

**参数：**此函数接受保存注释节点内容的单个参数**$data**。

**返回值：**此函数成功时返回新的 DOMComment 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createComment()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createComment() function to add a new comment node
$domComment = $domDocument->createComment('GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domComment);

// Save the XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<!--GeeksforGeeks-->

```

**程序 2：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createComment() function to add a new comment node
$domComment1 = $domDocument->createComment('Starting XML document file');
$domComment2 = $domDocument->createComment('Ending XML document file');

// Use createElement() function to add a new element node
$domElement1 = $domDocument->createElement('organization');
$domElement2 = $domDocument->createElement('name', 'GeeksforGeeks');
$domElement3 = $domDocument->createElement('address', 'Noida');
$domElement4 = $domDocument->createElement('email', 'abc@geeksforgeeks.org');

// Append element to the document
$domDocument->appendChild($domComment1);

$domDocument->appendChild($domElement1);
$domElement1->appendChild($domElement2);
$domElement1->appendChild($domElement3);
$domElement1->appendChild($domElement4);

$domDocument->appendChild($domComment2);

// Save the XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<!--Starting XML document file-->
<organization>
    <name>GeeksforGeeks</name>
    <address>Noida</address>
    <email>abc@geeksforgeeks.org</email>
</organization>
<!--Ending XML document file-->

```

**引用：**[https://www.php.net/manual/en/domdocument.createcomment.php](https://www.php.net/manual/en/domdocument.createcomment.php)
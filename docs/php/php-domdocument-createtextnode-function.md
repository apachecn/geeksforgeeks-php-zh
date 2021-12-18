# PHP|DOMDocument createTextNode()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createtextnode-function/](https://www.geeksforgeeks.org/php-domdocument-createtextnode-function/)

**DOMDocument：：createTextNode()函数**是 PHP 中的内置函数，用于创建 DOMText 类的新实例。

**语法：**

```php
*DOMText* DOMDocument::createTextNode( *string* $content )
```

**参数：**此函数接受保存文本内容的单个参数**$content**。

**返回值：**此函数成功时返回新的 DOMText 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createTextNode()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createTextNode() function to create text node
$domTN = $domDocument->createTextNode('GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domTN);

// Create XML document and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
GeeksforGeeks

```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createTextNode() function to create text node
$domTN1 = $domDocument->createTextNode("GeeksforGeeks");
$domTN2 = $domDocument->createTextNode("Noida");
$domTN3 = $domDocument->createTextNode("abc@geeksforgeeks.org");

// Append element to the document
$domDocument->appendChild($domTN1);
$domDocument->appendChild($domTN2);
$domDocument->appendChild($domTN3);

// Create XML document and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
GeeksforGeeks
Noida
abc@geeksforgeeks.org

```

**引用：**[https://www.php.net/manual/en/domdocument.createtextnode.php](https://www.php.net/manual/en/domdocument.createtextnode.php)
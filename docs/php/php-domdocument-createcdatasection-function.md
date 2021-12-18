# PHP|DOMDocument createCDATASection()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createcdatasection-function/](https://www.geeksforgeeks.org/php-domdocument-createcdatasection-function/)

**DOMDocument：：createCDATASection()函数**是 PHP 中的内置函数，用于创建 DOMCDATASection 类的新实例。

**语法：**

```php
*DOMCDATASection* DOMDocument::createCDATASection( *string* $data )
```

**参数：**此函数接受保存 CDATA 内容的单个参数**$data**。

**返回值：**此函数成功时返回新的 DOMCDATASection，失败时返回 False。

下面的程序说明了 PHP 中的 DOMDocument：：createCDATASection()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createCDATASection() function to create a new cdata node
$domElement = $domDocument->createCDATASection('GeeksforGeeks');

// Append element in the document
$domDocument->appendChild($domElement);

// Save the XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<![CDATA[GeeksforGeeks]]>

```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createComment() function to create a new comment node
$domComment = $domDocument->createComment('Create CDATA file');

// Use createCDATASection() function to create a new cdata node
$domElement = $domDocument->createCDATASection('GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domComment);
$domDocument->appendChild($domElement);

// Save the XML file and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<!--Create CDATA file-->
<![CDATA[GeeksforGeeks]]>

```

**引用：**[https://www.php.net/manual/en/domdocument.createcdatasection.php](https://www.php.net/manual/en/domdocument.createcdatasection.php)
# PHP|DOMDocument createEntityReference()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createentityreference-function/](https://www.geeksforgeeks.org/php-domdocument-createentityreference-function/)

**DOMDocument：：createEntityReference()函数**是 PHP 中的内置函数，用于创建 DOMEntityReference 类的新实例。

**语法：**

```php
*DOMEntityReference* DOMDocument::createEntityReference( *string* $name )
```

**参数：**此函数接受保存实体引用内容的单个参数**$name**。 实体引用不包含前导&和尾随；字符。

**返回值：**此函数成功时返回新的 DOMEntityReference 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createEntityReference()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument object
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createEntityReference() function to create
// new entity reference node
$domER = $domDocument->createEntityReference('nbsp');

// Append element to the document
$domDocument->appendChild($domER);

// Save the XML document and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
&nbsp;

```

**程序 2：**

```php
<?php

// Create a new DOMDocument object
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createEntityReference() function to create
// new entity reference node
$domER1 = $domDocument->createEntityReference('amp');
$domER2 = $domDocument->createEntityReference('lt');
$domER3 = $domDocument->createEntityReference('gt');
$domER4 = $domDocument->createEntityReference('reg');

// Append element to the document
$domDocument->appendChild($domER1);
$domDocument->appendChild($domER2);
$domDocument->appendChild($domER3);
$domDocument->appendChild($domER4);

// Save the XML document and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
&amp;
&lt;
&gt;
&reg;

```

**引用：**[https://www.php.net/manual/en/domdocument.createentityreference.php](https://www.php.net/manual/en/domdocument.createentityreference.php)
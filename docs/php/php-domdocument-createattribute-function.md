# PHP|DOMDocument createAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createattribute-function/](https://www.geeksforgeeks.org/php-domdocument-createattribute-function/)

**DOMDocument：：createAttribute()函数**是 PHP 中的内置函数，用于创建 DOMAttr 类的新实例。

**语法：**

```php
*DOMAttr* DOMDocument::createAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数成功时返回新的 DOMAttr 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：createAttribute()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createElement() function to create an element node
$domElement = $domDocument->createElement('organization',
                             'A computer science portal');

// Use createAttribute() function to create an attribute node
$domAttribute = $domDocument->createAttribute('name');

// Value of created attribute
$domAttribute->value = 'GeeksforGeeks';

// Append element to the document
$domElement->appendChild($domAttribute);

// Append it to the document itself
$domDocument->appendChild($domElement);

// Save the document into XML and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<organization name="GeeksforGeeks">A computer science portal</organization>

```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createElement() function to create an element node
$domElement = $domDocument->createElement('organization',
                                         'GeeksforGeeks');

$domAttribute1 = $domDocument->createAttribute('name');

// Value for the created attribute
$domAttribute1->value = 'GeeksforGeeks';

// Append element to the document
$domElement->appendChild($domAttribute1);

// Use createAttribute() function to create an attribute node
$domAttribute2 = $domDocument->createAttribute('address');

// Value for the created attribute
$domAttribute2->value = 'Noida';

// Append element to the document
$domElement->appendChild($domAttribute2);

// Use createAttribute() function to create an attribute node
$domAttribute3 = $domDocument->createAttribute('email');

// Value for the created attribute
$domAttribute3->value = 'abc@geeksforgeeks.org';

// Append element to the document
$domElement->appendChild($domAttribute3);

// Append it to the document itself
$domDocument->appendChild($domElement);

// Save the document to XML and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<organization name="GeeksforGeeks" address="Noida" email="abc@geeksforgeeks.org">
    GeeksforGeeks
</organization>

```

**引用：**[https://www.php.net/manual/en/domdocument.createattribute.php](https://www.php.net/manual/en/domdocument.createattribute.php)
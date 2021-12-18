# PHP|DOMDocument save()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-save-function/](https://www.geeksforgeeks.org/php-domdocument-save-function/)

**DOMDocument：：save()函数**是 PHP 中的一个内置函数，用于从 DOM 表示创建 XML 文档。 此函数在从头创建新 DOM 文档后使用。

**语法：**

```
*int* DOMDocument::save( *string* $filename, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename:** this parameter saves the path where the XML document is saved.
*   **$Options:** this parameter saves additional options. Currently, this parameter only supports LIBXML_NOEMPTYTAG.

**返回值：**此函数返回成功时写入的字节数，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：save()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Set the formatOutput to true
$domDocument->formatOutput = true;

// Create an element
$domElement = $domDocument->createElement('organization', 'GeeksforGeeks');

// Append element to the document
$domDocument->appendChild($domElement);

// Save the XML document
$domDocument->save("abcd.xml");

echo "File saved successfully";

?>
```

发帖主题：Re：Колибри0.7.8.0

**保存文件 abcd.xml 的内容：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<organization>GeeksforGeeks</organization>
```

**程序 2：**

```
<?php

// Create a new DOMDocument
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

// Save the XML file
$domDocument->save("g4g.xml");

echo "File saved successfully";

?>
```

发帖主题：Re：Колибри0.7.8.0

**保存文件 g4g.xml 的内容：**

```
<?xml version="1.0" encoding="iso-8859-1"?>
<organization>
    <name>GeeksforGeeks</name>
    <address>Noida</address>
    <email>abc@geeksforgeeks.org</email>
</organization>
```

**引用：**[https://www.php.net/manual/en/domdocument.save.php](https://www.php.net/manual/en/domdocument.save.php)
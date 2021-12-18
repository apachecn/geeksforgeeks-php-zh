# PHP|DOMDocument getElementsByTagName()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-getelementsbytagname-function/](https://www.geeksforgeeks.org/php-domdocument-getelementsbytagname-function/)

**DOMDocument：：getElementsByTagName()函数**是 PHP 中的内置函数，用于返回 DOMNodeList 类的新实例，该实例包含本地标记名的所有元素。

**语法：**

```php
*DOMNodeList* DOMDocument::getElementsByTagName( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存要匹配的本地标记名。 值*用于匹配所有标记。

**返回值：**此函数返回包含所有匹配元素的新 DOMNodeList 对象。

下面的程序演示了 PHP 中的 DOMDocument：：getElementsByTagName()函数：

**程序：**

```php
<?php

// Store the XML document to the variable
$xml = <<< XML
<?xml version="1.0" encoding="utf-8"?>
<organization>
    <name>GeeksforGeeks</name>
    <address>Noida India</address>
    <contact>
        <email>abc@geeksforgeeks.org</email>
        <mobile>+91-987654321</mobile>
    </contact>
</organization>
XML;

// Create new DOMDocument
$dom = new DOMDocument;

// Load the XML document
$dom->loadXML($xml);

// Use getElementsByTagName() function to search
// all elements with given local tag name
$org = $dom->getElementsByTagName('contact');

foreach ($org as $contact) {
    echo $contact->nodeValue, PHP_EOL;
}
?>
```

**输出：**

```php
abc@geeksforgeeks.org
+91-987654321

```

**引用：**[https://www.php.net/manual/en/domdocument.getelementsbytagname.php](https://www.php.net/manual/en/domdocument.getelementsbytagname.php)
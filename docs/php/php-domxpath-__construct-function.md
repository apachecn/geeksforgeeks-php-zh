# PHP|DOMXPath__Construction()函数

> Original: [https://www.geeksforgeeks.org/php-domxpath-__construct-function/](https://www.geeksforgeeks.org/php-domxpath-__construct-function/)

**DOMXPath：：__Construct()函数**是 PHP 中的内置函数，用于创建 DOMXPath 的实例。

**语法：**

```
*bool* DOMXPath::__construct( *DOMDocument* $doc )
```

**参数：**此函数接受单个参数**$doc**，该参数保存与 DOMXPath 关联的 DOMDocument。

下面的示例说明了 PHP 中的**DOMXPath：：__Construct()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<content>
  Hello World
</content>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Get the element
$tbody = $document->
getElementsByTagName('content')->item(0);

// Get the element with name content
$query = '//content';

// Evaluate the query
$entries = $xpath->evaluate($query, $tbody);
echo $entries[0]->nodeValue;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <content>
        First
    </content>
    <content>
        Second
    </content>
    <content>
        Third
    </content>
</root>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Get the root element
$tbody = $document->
getElementsByTagName('root')->item(0);

// Count the number of element with 
// name content
$query = 'count(//content)';

// Evaluate the query
$entries = $xpath->evaluate($query, $tbody);
echo $entries;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domxpath.construct.php](https://www.php.net/manual/en/domxpath.construct.php)
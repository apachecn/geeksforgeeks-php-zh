# PHP|DOMXPath registerNamespace()函数

> Original: [https://www.geeksforgeeks.org/php-domxpath-registernamespace-function/](https://www.geeksforgeeks.org/php-domxpath-registernamespace-function/)

**DOMXPath：：registerNamespace()函数**是 PHP 中的一个内置函数，用于向 DOMXPath 对象注册名称空间 URI 和前缀。

**语法：**

```
*bool* DOMXPath::registerNamespace( *string* $prefix,
                    *string* $namespaceURI )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$prefix:** it specifies the prefix.
*   **$NamespaceURI:** it specifies the namespace URI.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMXPath：：registerNamespace()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="UTF-8"?>
<body xmlns="geeksforgeeks" >
    <h1>Hello</h1>
</body>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Register namespace with prefix
// x and wrong URI
$xpath->registerNamespace('x',
              'geeksforgeeksnew');

// Use the prefix to create a query
// to get the text in h1
$query = '//x:body/x:h1/text()';

// Execute the query
$entries = $xpath->evaluate($query);

// Count the output
echo count($entries) . "\n";
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="UTF-8"?>
<body xmlns="geeksforgeeks" >
    <h1>Hello</h1>
</body>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Register namespace with prefix x
$xpath->registerNamespace('x',
               'geeksforgeeks');

// Use the prefix to create a query
// to get the text in h1
$query = '//x:body/x:h1/text()';

// Execute the query
$entries = $xpath->evaluate($query);

// View the text
echo $entries->item(0)->nodeValue . "\n";
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domxpath.registernamespace.php](https://www.php.net/manual/en/domxpath.registernamespace.php)
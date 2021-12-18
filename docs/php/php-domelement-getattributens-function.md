# PHP|DOMElement getAttributeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getattributens-function/](https://www.geeksforgeeks.org/php-domelement-getattributens-function/)

**DOMElement：：getAttributeNS()函数**是 PHP 中的一个内置函数，用于获取当前节点具有本地名称的特定命名空间中的属性值。

**语法：**

```
*string* DOMElement::getAttributeNS( *string* $namespaceURI, 
*string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI:** it specifies the namespace URI.
*   **$localName:** it specifies the local name.

**返回值：**此函数返回包含属性值的字符串值，如果未找到具有给定 localName 和名称空间 URI 的属性，则返回空字符串。

以下示例说明 PHP 中的**DOMElement：：getAttributeNS()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<body xmlns:x=\"my_namespace\">
    <x:div x:attr=\"value\" > DIV 1 </x:div>
</body>");

// Get the elements by tagname
$elements = $dom->getElementsByTagName('div');

// Get the attribute node value
$nodeValue = $elements[0]->getAttributeNS('my_namespace', 'attr');

echo $nodeValue;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
<body xmlns:x=\"my_namespace1\">
    <x:div x:id=\"my_id1\" > DIV 1 </x:div>
    <x:div x:id=\"my_id2\" > DIV 1 </x:div>
</body>
<body xmlns:xi=\"my_namespace2\">
    <xi:div xi:id=\"new\" > DIV 1 </xi:div>
</body>
</root>");

// Get the elements by tagname
$elements = $dom->getElementsByTagName('div');

foreach ($elements as $element) {

    // Get node value only from my_namespace1
    $nodeValue = $element->getAttributeNS('my_namespace1', 'id');

    if ($nodeValue) {
       echo $nodeValue . '<br>';
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.getattributens.php](https://www.php.net/manual/en/domelement.getattributens.php)
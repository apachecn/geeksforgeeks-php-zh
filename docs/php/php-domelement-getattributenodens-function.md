# PHP|DOMElement getAttributeNodeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getattributenodens-function/](https://www.geeksforgeeks.org/php-domelement-getattributenodens-function/)

**DOMElement：：getAttributeNodeNS()函数**是 PHP 中的一个内置函数，用于获取当前节点具有本地名称的特定名称空间中的属性节点。

**语法：**

```php
*DOMAttr* DOMElement::getAttributeNodeNS( *string* $namespaceURI, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI:** it specifies the namespace URI.
*   **$localName:** it specifies the local name.

**返回值：**此函数返回包含属性节点的属性值。

下面给出的程序演示了 PHP 中的**DOMElement：：getAttributeNodeNS()函数**：

**程序 1：**

```php
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

// Get the attribute node
$node = $elements[0]->getAttributeNodeNS('my_namespace', 'attr');

// Extract name
$name = $node->name;

// Extract value
$value = $node->value;

echo $name . " => " . $value . "<br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
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

    $node = $element->getAttributeNodeNS('my_namespace1', 'id');

    if ($node) {

        // Extract name
        $name = $node->name;

        // Extract value
        $value = $node->value;

        echo $name . " => " . $value . "<br>";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.getattributenodens.php](https://www.php.net/manual/en/domelement.getattributenodens.php)
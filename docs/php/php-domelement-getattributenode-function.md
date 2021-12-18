# PHP|DOMElement getAttributeNode()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getattributenode-function/](https://www.geeksforgeeks.org/php-domelement-getattributenode-function/)

**DOMElement：：getAttributeNode()函数**是 PHP 中的一个内置函数，用于获取当前元素的带有名称的属性节点。

**语法：**

```php
*DOMAttr* DOMElement::getAttributeNode( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数返回包含属性节点的 DOMAttr 值。

以下示例说明 PHP 中的**DOMElement：：getAttributeNode()函数**：

**示例 1：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<body>
    <div attr=\"value\"> DIV 1 </div>
</body>");

// Get the elements by tagname
$elements = $dom->getElementsByTagName('div');

// Get the attribute node
$node = $elements[0]->getAttributeNode('attr');

// Extract name
$name = $node->name;

// Extract value
$value = $node->value;

echo $name . " => " . $value . "<br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<body>
    <div id=\"div1\"> DIV 1 </div>
    <div id=\"div2\"> DIV 2 </div>
    <div id=\"div3\"> DIV 3 </div>
</body>");

// Get the elements by tagname
$elements = $dom->getElementsByTagName('div');

// Get the id of a element
echo "All the divs with id values are: <br>";
foreach ($elements as $element) {
    // Get the attribute node
    $node = $element->getAttributeNode('id');

    // Extract name
    $name = $node->name;

    // Extract value
    $value = $node->value;

    echo $name . " => " . $value . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.getattributenode.php](https://www.php.net/manual/en/domelement.getattributenode.php)
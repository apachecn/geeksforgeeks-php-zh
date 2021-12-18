# PHP|DOMElement setAttributeNodeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-setattributenodens-function/](https://www.geeksforgeeks.org/php-domelement-setattributenodens-function/)

**DOMElement：：setAttributeNodeNS()函数**是 PHP 中的内置函数，用于向元素添加新的属性节点。 这只是*setAttributeNode()*函数的替代方法。

**语法：**

```
*DOMAttr* DOMElement::setAttributeNodeNS( *DOMAttr* $attr )
```

**参数：**此函数接受单个参数**$attr**，该参数保存要添加的属性。

**返回值：**如果属性已被替换，则此函数返回旧节点。

**异常：**如果节点为只读，则此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR。

以下示例说明 PHP 中的**DOMElement：：setAttributeNodeNS()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a element with a namespace
$root = $dom->createElementNS("my_namepsace", "root");

// Create an element
$node = $dom->createElement("div", "GeeksforGeeks");

// Append the child
$dom->appendChild($root);

// Add the node to the dom
$newnode = $dom->appendChild($node);

// Create a DOMAttr instance
$attr = new DOMAttr('style', 'color: green; font-size: 100px;');

// Set the attribute
$newnode->setAttributeNodeNS($attr);

echo $dom->saveXML();
?>
```

**输出：**
![](img/9db7dfbc8f4a76dfc4a254071af4688f.png)

**示例 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"my_id\"> Geeksforgeeks </h1>
        <h2> Second heading </h2>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

echo "Before the addition of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;

// Create a DOMAttr instance
$attr = new DOMAttr('class', 'value');

// Add the new attribute
$node->setAttributeNodeNS($attr);

echo "<br>After the addition of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.0

```
Before the addition of attributes:
No of attributes => 1
After the addition of attributes:
No of attributes => 2
```

**引用：**[https://www.php.net/manual/en/domelement.setattributenodens.php](https://www.php.net/manual/en/domelement.setattributenodens.php)
# PHP|DOMElement setAttributeNode()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-setattributenode-function/](https://www.geeksforgeeks.org/php-domelement-setattributenode-function/)

**DOMElement：：setAttributeNode()函数**是 PHP 中的内置函数，用于向元素添加新的属性节点。

**语法：**

```
*DOMAttr* DOMElement::setAttributeNode( *DOMAttr* $attr )
```

**参数：**此函数接受单个参数**$attr**，该参数保存要添加的属性节点。

**返回值：**如果 DOMAttr 值已被替换或为空，则此函数返回包含旧节点的 DOMAttr 值。

**异常：**如果节点为只读，则此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR。

下面给出的程序演示了 PHP 中的**DOMElement：：setAttributeNode()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create an element
$node = $dom->createElement("p", 'GeeksforGeeks');

// Add the node to the dom
$newnode = $dom->appendChild($node);

// Create a DOMAttr instance which
// increase the font-size
$attr = new DOMAttr('style', 'font-size: 80px;');

// Set the attribute
$newnode->setAttributeNode($attr);

// View the XML
echo $dom->saveXML();
?>
```

发帖主题：Re：Колибри0.7.0

```
<?xml version="1.0"?>
<p style="font-size: 80px;">GeeksforGeeks</p>
```

![](img/227503dbb758e2fee59d0e04930c8484.png)

**程序 2：**

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
$node->setAttributeNode($attr);

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

**引用：**[https://www.php.net/manual/en/domelement.setattributenode.php](https://www.php.net/manual/en/domelement.setattributenode.php)
# PHP|DOMNamedNodeMap getNamedItemNS()函数

> Original: [https://www.geeksforgeeks.org/php-domnamednodemap-getnameditemns-function/](https://www.geeksforgeeks.org/php-domnamednodemap-getnameditemns-function/)

**DOMNamedNodeMap：：getNamedItemNS()函数**是 PHP 中的一个内置函数，用于检索具有特定本地名称和命名空间 URI 的节点。 此函数可用于从特定命名空间获取属性的值。

**语法：**

```
*DOMNode* DOMNamedNodeMap::getNamedItemNS
( *string* $namespaceURl, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURl:** it specifies the namespace URI.
*   **$localName:** it specifies the local name.

**返回值：**此函数返回具有给定本地名称和命名空间 URI 的节点。

下面给出的程序演示了 PHP 中的**DOMNamedNodeMap：：getNamedItemNS()函数**：

**程序 1：**在本例中，我们将获得具有两个不同名称空间的元素的属性值。

```
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Create an element with namespace
$node = $dom->createElementNS(
   "my_namespace", "x:p", 'Hello, this is my paragraph.');

// Add the node to the dom
$newnode = $dom->appendChild($node);

// Set the attribute with a namespace
$newnode->setAttributeNS("my_namespace", "style", "color:blue");

echo "<b>Attributes with my_namespace as namespace:</b> <br>";

// Get the attribute value
$attribute = 
   $node->attributes->getNamedItemNS('my_namespace', 'style')->nodeValue;
echo $attribute;

echo "<br><b>Attributes with other_namespace as namespace:</b> <br>";

// Get the attribute value
$attribute = 
   $node->attributes->getNamedItemNS('other_namespace', 'style')->nodeValue;
echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**在本例中，我们将通过更改属性的值来检查函数是否获取最新属性值。

```
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Create an element
$node = $dom->createElementNS("my_namespace", "x:p", 'GeeksforGeeks');

// Add the node to the dom
$newnode = $dom->appendChild($node);

// Set the attribute with a namespace
$newnode->setAttributeNS("my_namespace", "style", "color:blue");

echo "<b>Before:</b> <br>";

// Get the attribute value
$attribute = 
    $node->attributes->getNamedItemNS('my_namespace', 'style')->nodeValue;
echo $attribute;

// Change the attribute value 
$newnode->setAttributeNS("my_namespace", "style", "color:red");

echo "<br><b>After:</b> <br>";

// Get the attribute value
$attribute = 
    $node->attributes->getNamedItemNS('my_namespace', 'style')->nodeValue;
echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnamednodemap.getnameditemns.php](https://www.php.net/manual/en/domnamednodemap.getnameditemns.php)
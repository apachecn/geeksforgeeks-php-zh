# PHP|DOMNamedNodeMap Item()函数

> Original: [https://www.geeksforgeeks.org/php-domnamednodemap-item-function/](https://www.geeksforgeeks.org/php-domnamednodemap-item-function/)

**DOMNamedNodeMap：：Item()函数**是 PHP 中的内置函数，用于检索 index 指定的节点。 此函数用于从元素中获取特定属性，进而可以根据需要获取该属性的名称或值。

**语法：**

```
*DOMNamedNodeMap* DOMNamedNodeMap::item( *int* $index )
```

**参数：**此函数接受保存索引的单个参数**$index**。

**返回值：**此函数返回地图中索引位置处的节点。

下面给定的程序说明了 PHP：
**程序 1：**中的**DOMNamedNodeMap：：Item()函数**。在此示例中，我们将使用 index()获取属性的名称

```
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"first\" 
            class=\"first\" attrib=\"attrib_value\"> Geeksforgeeks </h1>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

// Get the 2nd attribute's value
$attribute1 = $node->attributes->item(0)->nodeName;
$attribute2 = $node->attributes->item(1)->nodeName;
$attribute3 = $node->attributes->item(2)->nodeName;
echo "$attribute1, $attribute2 and $attribute3";
?>
```

发帖主题：Re：Колибри0.7.0

```
id, class and attrib
```

**程序 2：**在本例中，我们将使用 index()获取属性的值

```
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"first\" 
            class=\"geeksforgeeks\" attrib=\"attrib_value\"> Geeksforgeeks </h1>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

// Get the 2nd attribute's value
$attribute1 = $node->attributes->item(0)->nodeValue;
$attribute2 = $node->attributes->item(1)->nodeValue;
$attribute3 = $node->attributes->item(2)->nodeValue;
echo "$attribute1, $attribute2 and $attribute3";
?>
```

发帖主题：Re：Колибри0.7.0

```
first, geeksforgeeks and attrib_value
```

**引用：**[https://www.php.net/manual/en/domnamednodemap.item.php](https://www.php.net/manual/en/domnamednodemap.item.php)
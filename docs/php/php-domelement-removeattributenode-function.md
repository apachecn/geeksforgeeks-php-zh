# PHP|DOMElement removeAttributeNode()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-removeattributenode-function/](https://www.geeksforgeeks.org/php-domelement-removeattributenode-function/)

**DOMElement：：removeAttributeNode()函数**是 PHP 中的一个内置函数，用于从元素中删除属性。

**语法：**

```php
*bool* DOMElement::removeAttributeNode( *DOMAttr* $oldnode )
```

**参数：**此函数接受单个参数**$oldnode**，该参数保存要删除的属性。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**如果节点是只读的，则此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR，如果**$oldnode**不是元素的属性，则抛出 DOM_NOT_FOUND_ERROR。

下面给出的程序演示了 PHP 中的**DOMElement：：removeAttributeNode()函数**：

**程序 1：**

```php
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

echo "Before the removal of attributes: <br>";

// Get the attribute name and value
$attribute = $node->attributes->item(0);
$attribute_name = $attribute->name;
$attribute_value = $attribute->value;

echo $attribute_name . ' => ';
echo $attribute_value;

// Get the attribute to remove
$oldnode = $node->getAttributeNode('id');

// Remove the id attribute
$node->removeAttributeNode($oldnode);

echo "<br>After the removal of attributes: <br>";

// Get the attribute name and value
$attribute = $node->attributes->item(0);
$attribute_name = $attribute->name . ' => ';
$attribute_value = $attribute->value;
echo $attribute_name;
echo $attribute_value;
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
    <html>
        <h1 id=\"my_id\" style=\"color:green;\" 
          class=\"my_class\"> Geeksforgeeks </h1>
        <h2> Second heading </h2>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

echo "Before the removal of attributes: <br>";

// Get the attribute to remove
$oldnode = $node->getAttributeNode('id');

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;

// Remove the id attribute
$node->removeAttributeNode($oldnode);

echo "<br>After the removal of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.removeattributenode.php](https://www.php.net/manual/en/domelement.removeattributenode.php)
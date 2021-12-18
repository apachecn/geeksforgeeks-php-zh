# PHP|DOMElement removeAttributeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-removeattributens-function/](https://www.geeksforgeeks.org/php-domelement-removeattributens-function/)

**DOMElement：：removeAttributeNS()函数**是 PHP 中的一个内置函数，用于从元素中删除特定名称空间中具有特定本地名称的属性。

**语法：**

```
*bool* DOMElement::removeAttributeNS( *string* $namespaceURI, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI:** it specifies the namespace URI.
*   **$localName:** it specifies the local name.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**当节点为只读时，此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR。

以下示例说明 PHP 中的**DOMElement：：removeAttributeNS()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html xmlns:x=\"my_namespace\">
        <x:h1 x:id=\"my_id\"> Geeksforgeeks </x:h1>
        <x:h2> Second heading </x:h2>
    </html>
    <html xmlns:y=\"another_namespace\">
        <y:h1 id=\"my_new_id\"> Random text </y:h1>
        <y:h2> Another heading </y:h2>
    </html>
</root>");

// Get the elements
$nodes = $dom->getElementsByTagName('h1');

echo "Before the removal of attributes: <br>";

foreach ($nodes as $node) {

    // Get the attribute name and value
    $attribute = $node->attributes->item(0);
    $attribute_name = $attribute->name;
    $attribute_value = $attribute->value;

    echo $attribute_name . ' => ';
    echo $attribute_value . '<br>';

    // Remove the id attribute
    $node->removeAttributeNS('my_namespace', 'id');
}

echo "<br>After the removal of attributes: <br>";

foreach ($nodes as $node) {
    // Get the attribute name and value
    $attribute = $node->attributes->item(0);
    $attribute_name = $attribute->name;
    $attribute_value = $attribute->value;
    echo $attribute_name . ' => ';
    echo $attribute_value . '<br>';
}
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
    <html xmlns:x=\"my_namespace\">
        <x:h1 x:id=\"my_id\"> 
        Geeksforgeeks 
        </x:h1>
        <x:h2> Second heading </x:h2>
    </html>
    <html xmlns:y=\"another_namespace\">
        <y:h1 y:id=\"my_new_id\" 
         y:style=\"color: blue;\">
         Random text 
         </y:h1>
        <y:h2> Another heading </y:h2>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[1];

echo "Before the removal of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;

// Remove the id attribute
$node->removeAttributeNS('another_namespace', 'id');

echo "<br>After the removal of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.removeattributens.php](https://www.php.net/manual/en/domelement.removeattributens.php)
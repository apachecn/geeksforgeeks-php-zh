# PHP|DOMElement removeAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-removeattribute-function/](https://www.geeksforgeeks.org/php-domelement-removeattribute-function/)

**DOMElement：：removeAttribute()函数**是 PHP 中的一个内置函数，用于从元素中删除具有特定名称的属性。

**语法：**

```php
*bool* DOMElement::removeAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**如果节点为只读，则此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR。

以下示例说明 PHP 中的**DOMElement：：removeAttribute()函数**：

**示例 1：**

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

// Remove the id attribute
$node->removeAttribute('id');

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

**示例 2：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"my_id\" 
            style=\"color:green;\" 
            class=\"my_class\"> 
            Geeksforgeeks 
        </h1>
        <h2> Second heading </h2>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

echo "Before the removal of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;

// Remove the id attribute
$node->removeAttribute('id');

echo "<br>After the removal of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.removeattribute.php](https://www.php.net/manual/en/domelement.removeattribute.php)
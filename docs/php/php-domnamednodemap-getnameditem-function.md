# PHP|DOMNamedNodeMap getNamedItem()函数

> Original: [https://www.geeksforgeeks.org/php-domnamednodemap-getnameditem-function/](https://www.geeksforgeeks.org/php-domnamednodemap-getnameditem-function/)

**DOMNamedNodeMap：：getNamedItem()函数**是 PHP 中的内置函数，用于检索由名称指定的节点。 这用于获取属性项，并进一步获取有关属性的信息。

**语法：**

```php
*DOMNode* DOMNamedNodeMap::getNamedItem( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存要检索的节点的*nodeName*。

**返回值：**成功时，此函数返回指定名称的 DOMNode。

以下示例说明 PHP 中的**DOMNamedNodeMap：：getNamedItem()函数**：

**示例 1：**在此示例中，我们将获取元素的属性值。

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"first\" 
            class=\"first\" 
            style=\"color: blue\"> 
         Geeksforgeeks 
        </h1>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

// Get the attribute value
$attribute = $node->attributes->
    getNamedItem('style')->nodeValue;
echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在此示例中，我们将通过更改属性的值来检查函数是否获取最新属性值。

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <html>
        <h1 id=\"first\" 
            class=\"first\">
         Geeksforgeeks 
        </h1>
        <h2> Second heading </h2>
    </html>
</root>");

// Get the elements
$node = $dom->getElementsByTagName('h1')[0];

echo "Before: <br>";

// Get the attribute value
$attribute = $node->attributes->
     getNamedItem('class')->nodeValue;
echo $attribute;

// Change the value of attribute
$node->setAttribute('class', 'changed');

echo "<br>After: <br>";

// Get the attribute value
$attribute = $node->attributes->
    getNamedItem('class')->nodeValue;
echo $attribute;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnamednodemap.getnameditem.php](https://www.php.net/manual/en/domnamednodemap.getnameditem.php)
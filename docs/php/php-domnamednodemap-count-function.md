# PHP|DOMNamedNodeMap count()函数

> Original: [https://www.geeksforgeeks.org/php-domnamednodemap-count-function/](https://www.geeksforgeeks.org/php-domnamednodemap-count-function/)

**DOMNamedNodeMap：：count()函数**是 PHP 中的一个内置函数，用于获取映射中的节点数。 它可用于计算元素的属性。

**语法：**

```
*int* DOMNamedNodeMap::count( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含映射中节点数的整数值。

下面的示例说明了 PHP 中的**DOMNamedNodeMap：：count()函数**：

**示例 1：**在此示例中，我们将计算元素的属性。

```
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

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在本例中，我们将检查 COUNT 函数是否通过更改属性数来获取最新的属性数。

```
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

echo "Before the addition of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;

// Set the id attribute
$node->setAttribute('new', 'value');

echo "<br>After the addition of attributes: <br>";

// Get the attribute count
$attributeCount = $node->attributes->count();
echo 'No of attributes => ' . $attributeCount;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnamednodemap.count.php](https://www.php.net/manual/en/domnamednodemap.count.php)
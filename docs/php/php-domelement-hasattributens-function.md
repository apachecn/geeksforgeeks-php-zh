# PHP|DOMElement hasAttributeNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-hasattributens-function/](https://www.geeksforgeeks.org/php-domelement-hasattributens-function/)

**DOMElement：：hasAttributeNS()函数**是 PHP 中的一个内置函数，用于知道名为 localName 的特定命名空间中的属性是否作为元素的成员存在。

**语法：**

```php
*bool* DOMElement::hasAttributeNS( *string* $namespaceURI, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI:** it specifies the namespace URI.
*   **$localName:** it specifies the local name.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

以下示例说明 PHP 中的**DOMElement：：hasAttributeNS()函数**：

**示例 1：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <div xmlns:x=\"my_namespace\">
        <x:h1 x:style=\"color:red;\">
        Hello, this is my red heading.
        </x:h1>
        <x:h1 x:style=\"color:green;\">
        Hello, this is my green heading. 
        </x:h1>
        <x:h1 x:style=\"color:blue;\"> 
        Hello, this is my blue heading.
        </x:h1>
    </div>
    <div xmlns:y=\"another_namespace\">
        <y:h1> Hello, this is my new red heading. </y:h1>
        <y:h1> Hello, this is my new green heading. </y:h1>
        <y:h1> Hello, this is my new blue heading. </y:h1>
    </div>
</root>");

// Get the elements
$nodeList = $dom->getElementsByTagName('h1');

$i = 0;

foreach ($nodeList as $node) {
    if($node->hasAttributeNS('my_namespace', 'style')) {
        $i++;
    }
}
echo "Yes, there are total of $i style 
               attributes inside my_namespace";
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
    <div xmlns:x=\"my_namespace\">
        <x:h1 x:id=\"color:red;\"> 1 </x:h1>
        <x:h1 x:id=\"color:green;\"> 2 </x:h1>
        <x:h1 x:id=\"color:blue;\"> 3 </x:h1>
    </div>
    <div xmlns:y=\"another_namespace\">
        <y:h1> 1 </y:h1>
        <y:h1> 2 </y:h1>
        <y:h1> 3 </y:h1>
    </div>
</root>");

// Get the elements
$nodeList = $dom->getElementsByTagName('h1');

$i = 0;

foreach ($nodeList as $node) {
    if($node->hasAttributeNS('another_namespace', 'id')) {
        $i++;
    }
}
echo "There are total of $i id attributes
                         inside another_namespace.";
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.hasattributens.php](https://www.php.net/manual/en/domelement.hasattributens.php)
# PHP|DOMElement hasAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-hasattribute-function/](https://www.geeksforgeeks.org/php-domelement-hasattribute-function/)

**DOMElement：：hasAttribute()函数**是 PHP 中的一个内置函数，用于知道具有特定名称的属性是否作为元素的成员存在。

**语法：**

```php
*bool* DOMElement::hasAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMElement：：hasAttribute()函数**：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <div>
        <!-- id attribute is there -->
        <p id=\"prog\"> HELLO </p>
    </div>
</root>");

// Get the elements
$nodeList = $dom->getElementsByTagName('p');

foreach ($nodeList as $node) {
    if($node->hasAttribute('id')) {
        echo "Yes, id attribute is there.";
    }
}
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
    <div>
        <!-- id attribute is missing -->
        <p> HELLO </p>
    </div>
</root>");

// Get the elements
$nodeList = $dom->getElementsByTagName('p');
foreach ($nodeList as $node) {
    if(!$node->hasAttribute('id')) {
        echo "No, id attribute isn't there.";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.hasattribute.php](https://www.php.net/manual/en/domelement.hasattribute.php)
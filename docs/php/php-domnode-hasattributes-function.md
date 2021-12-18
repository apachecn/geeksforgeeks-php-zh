# PHP|DOMNode hasAttributes()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-hasattributes-function/](https://www.geeksforgeeks.org/php-domnode-hasattributes-function/)

**DOMNode：：hasAttributes()函数**是 PHP 中的一个内置函数，用于检查节点是否有属性。

**语法：**

```
*bool* DOMNode::hasAttributes( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

以下示例说明 PHP 中的**DOMNode：：hasAttributes()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element
$element = $dom->createElement('p',
      'This is the paragraph element!');

// Set the attribute
$element->setAttribute('id', 'my_id');

// Append the child
$dom->appendChild($element);

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

**示例 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element
$element = $dom->createElement('p', 
         'This is the paragraph element!');

// Set the attribute
$element->setAttribute('class', 'my_class');

// Append the child
$dom->appendChild($element);

// Get the elements
$nodeList = $dom->getElementsByTagName('p');
foreach ($nodeList as $node) {
    if(!$node->hasAttribute('id')) {
        echo "No, id attribute is not there.";
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.hasattributes.php](https://www.php.net/manual/en/domnode.hasattributes.php)
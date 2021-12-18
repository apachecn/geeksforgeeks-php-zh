# PHP|DOMNodeList Item()函数

> Original: [https://www.geeksforgeeks.org/php-domnodelist-item-function/](https://www.geeksforgeeks.org/php-domnodelist-item-function/)

**DOMNodeList：：Item()函数**是 PHP 中的内置函数，用于检索 index 指定的节点。

**语法：**

```php
*DOMNode* DOMNodeList::item( *int* $index )
```

**参数：**此函数接受保存索引的单个参数**$index**。

**返回值：**此函数返回索引指定的 DOMNode。

下面的示例说明了 PHP 中的**DOMNodeList：：Item()函数**：

**示例 1：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a div element
$element = $document->appendChild(new DOMElement('div'));

// Create a h1 element
$text1 = new DOMElement('h1', 'GeeksforGeeks');

// Create another h1 elements
$text2 = new DOMElement('h1', 'Another GeeksforGeeks');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

// Get all elements with tag name 'h1'
$elements = $document->getElementsByTagName('h1');

// Get the text of first element
echo $elements->item(0)->textContent;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a div element
$element = $document->appendChild(new DOMElement('div'));

// Create a h1 element
$text1 = new DOMElement('h1', 'GeeksforGeeks');

// Create another h1 elements
$text2 = new DOMElement('h2', 'Another GeeksforGeeks');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

// Get all elements
$elements = $document->getElementsByTagName('*');

// Get the name of tag of third element
echo $elements->item(2)->nodeName;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnodelist.item.php](https://www.php.net/manual/en/domnodelist.item.php)
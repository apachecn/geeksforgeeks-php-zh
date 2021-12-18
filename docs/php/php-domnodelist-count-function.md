# PHP|DOMNodeList count()函数

> Original: [https://www.geeksforgeeks.org/php-domnodelist-count-function/](https://www.geeksforgeeks.org/php-domnodelist-count-function/)

**DOMNodeList：：count()函数**是 PHP 中的一个内置函数，用于获取列表中的节点数。

**语法：**

```php
*int* DOMNodeList::count( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回列表中的节点数。

下面的示例说明了 PHP 中的**DOMNodeList：：Count()函数**：

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

// Count the elements
echo $elements->count();
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
$text2 = new DOMElement('h1', 'Another GeeksforGeeks');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

// Get all elements with tag name 'h1'
$elements = $document->getElementsByTagName('h1');

// Count the elements
echo 'Before removing: ';
echo $elements->count() . "<br>";

// Remove  a child
$element->removeChild($text2);

// Get all elements with tag name 'h1'
$elements = $document->getElementsByTagName('h1');

// Count the elements
echo 'After removing: ';
echo $elements->count();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnodelist.count.php](https://www.php.net/manual/en/domnodelist.count.php)
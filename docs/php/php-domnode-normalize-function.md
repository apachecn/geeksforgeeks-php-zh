# PHP|DOMNode Normize()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-normalize-function/](https://www.geeksforgeeks.org/php-domnode-normalize-function/)

**DOMNode：：Normize()函数**是 PHP 中的一个内置函数，用于删除空文本节点并合并该节点及其所有子节点中的相邻文本节点。

**语法：**

```php
*void* DOMNode::normalize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的示例说明了 PHP 中的**DOMNode：：Normal ize()函数**：

**示例 1：**在本程序中，我们将展示 Normize 如何删除空文本节点。

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a div element
$element = $document->
    appendChild(new DOMElement('div'));

// Create a text Node
$text1 = $document->
    createTextNode('GeeksforGeeks');

// Create a empty text Node
$text2 = $document->createTextNode('');

// Create another empty text Node
$text3 = $document->createTextNode('');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);
$element->appendChild($text3);

echo "Number of text nodes before normalization: ";
echo count($element->childNodes) . "<br>";

// Normalize the document
$document->normalize();

echo "Number of text nodes after normalization: ";
echo count($element->childNodes);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在本程序中，我们将展示 Normize 如何合并所有相邻文本节点。

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a div element
$element = $document->
    appendChild(new DOMElement('div'));

// Create a text Node
$text1 = $document->
               createTextNode('Hello');

// Create another text Node
$text2 = $document->
               createTextNode('World');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

echo "Number of text nodes "
                . "before normalization: ";
echo count($element->childNodes) . "<br>";

// Normalize the document
$document->normalize();

echo "Number of text nodes after "
                         . "normalization: ";
echo count($element->childNodes);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.normalize.php](https://www.php.net/manual/en/domnode.normalize.php)
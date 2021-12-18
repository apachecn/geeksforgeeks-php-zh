# PHP|DOMNode replaceChild()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-replacechild-function/](https://www.geeksforgeeks.org/php-domnode-replacechild-function/)

**DOMNode：：replaceChild()函数**是 PHP 中的一个内置函数，用于用传递的新节点替换旧的子节点。 此外，如果新节点已经是子节点，则不会第二次添加该节点。 如果替换成功，则返回旧节点。

**语法：**

```php
*DOMNode* DOMNode::replaceChild( *DOMNode* $newnode, *DOMNode* $oldnode )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$newnode:** it specifies the new node.
*   **$oldnode:** it specifies the old node.

**返回值：**此函数返回旧节点，如果出现错误，则返回 False。

**异常：**此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR，如果此节点是只读的，或者如果要插入的节点的上一个父节点是只读的，DOM_HERHORY_REQUEST_ERR，如果此节点的类型不允许**$newnode**节点的子节点，或者如果要放入的节点是此节点的祖先之一或此节点本身，则抛出 DOM_WRONG_DOCUMENT_ERR， 如果**$newnode**是从与创建此节点的文档 DOM_NOT_FOUND 不同的文档创建的，如果**$oldnode**不是此节点的子节点。

下面的示例说明了 PHP 中的**DOMNode：：replaceChild()函数**：

**程序 1：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a root element
$element = $document->appendChild(new DOMElement('root'));

// Create the text Node
$text1 = $document->createTextNode('Hello ! ');
$text2 = $document->createTextNode('Text to be replaced');
$text3 = $document->createTextNode('replaced');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

// Replace the child
$element->replaceChild($text3, $text2);

// Render the output
echo $document->saveXML();
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a h1 element
$element = $document->appendChild(new DOMElement('h1'));

// Create the text Node
$text1 = $document->createTextNode('Geeksfor');
$text2 = $document->createTextNode('Text to be removed');
$text3 = $document->createTextNode('Geeks');

// Append the nodes
$element->appendChild($text1);
$element->appendChild($text2);

// Replace the child
$element->replaceChild($text3, $text2);

// Render the output
echo $document->saveXML();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.replacechild.php](https://www.php.net/manual/en/domnode.replacechild.php)
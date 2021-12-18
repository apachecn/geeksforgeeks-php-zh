# PHP|DOMText plitText()函数

> Original: [https://www.geeksforgeeks.org/php-domtext-splittext-function/](https://www.geeksforgeeks.org/php-domtext-splittext-function/)

**DOMText：：plitText()函数**是 PHP 中的一个内置函数，用于在指定偏移量处将一个节点拆分为两个节点。

**语法：**

```
*DOMText* DOMText::splitText( *int* $offset )
```

**参数：**此函数接受单个参数**$Offset**，该参数保存要拆分的偏移量。

**返回值：**此函数返回相同类型的新节点，该节点包含偏移量及其之后的所有内容。

下面给出的程序演示了 PHP 中的**DOMText：：plitText()函数**：

**程序 1：**

```
<?php

// Create the text Node
$text = new DOMText('GeeksforGeeks');

// Split the text
$splitedtext = $text->splitText(8);
echo $splitedtext->nodeValue;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a div element
$element = $document->appendChild(new DOMElement('div'));

// Create a text Node
$text = $document->createTextNode('GeeksforGeeks');

// Append the nodes
$element->appendChild($text);

echo "Number of text nodes before splitting: ";
echo count($element->childNodes) . "<br>";

// Splitting the text
$text->splitText(5);

echo "Number of text nodes after splitting: ";
echo count($element->childNodes);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domtext.splittext.php](https://www.php.net/manual/en/domtext.splittext.php)
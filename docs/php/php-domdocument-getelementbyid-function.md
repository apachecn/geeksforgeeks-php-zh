# PHP|DOMDocument getElementById()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-getelementbyid-function/](https://www.geeksforgeeks.org/php-domdocument-getelementbyid-function/)

**DOMDocument：：getElementById()函数**是 PHP 中的一个内置函数，用于搜索具有特定 id 的元素。

**语法：**

```php
*DOMElement* DOMDocument::getElementById( *string* $elementId )
```

**参数：**此函数接受单个参数**$elementId**，该参数保存要搜索的 id。

**返回值：**此函数返回 DOMElement，如果未找到元素，则返回 NULL。

下面给出的程序演示了 PHP 中的**DOMDocument：：getElementById()函数**：

**程序 1：**在本程序中，我们将获得具有特定 id 的元素的标记名。

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div'));

// Create a id attribute to div
$attr = $element->setAttributeNode(
        new DOMAttr('id', 'my_id'));

// Set that attribute as id
$element->setIDAttribute('id', true);

// Get the tag name
$tagname = $dom->getElementById('my_id')->tagName;

echo $tagname;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**在本程序中，我们将获取具有一定 id 的元素的内容。

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div',
   'Hey, this is the text content of the div element.'));

// Create a id attribute to div
$attr = $element->setAttributeNode(
          new DOMAttr('id', 'my_id'));

// Set that attribute as id
$element->setIDAttribute('id', true);

// Get the tag content
$tagcontent = $dom->getElementById('my_id')->textContent;

echo $tagcontent;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.getelementbyid.php](https://www.php.net/manual/en/domdocument.getelementbyid.php)
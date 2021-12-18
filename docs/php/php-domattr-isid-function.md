# PHP|DOMAttr ISID()函数

> Original: [https://www.geeksforgeeks.org/php-domattr-isid-function/](https://www.geeksforgeeks.org/php-domattr-isid-function/)

**DOMAttr：：isid()函数**是 PHP 中的一个内置函数，用于检查属性是否为定义的 ID。 根据 DOM 标准，它要求属性 ID 的类型为 ID。在使用此函数之前，您需要使用*DOMDocument：：validateOnParse()方法*验证您的文档。

**语法：**

```php
*bool* DOMAttr::isId( *void* )
```

**参数：**此函数不接受任何参数。
**返回值：**如果该函数包含 id 属性，则返回 TRUE，否则返回 FALSE。

下面给出的程序说明了 PHP 中的**DOMAttr：：isid()函数**：

**程序 1：**

## PHP

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div'));

// Create a class attribute
$attr = $element->setAttributeNode(
        new DOMAttr('class', 'geekforgeeks'));

// Get the attribute
$getattr = $dom->getElementsByTagName('div')
        ->item(0)->getAttributeNode('class');

// Check if it is id or not
if($getattr->isId()) {
    echo 'Yes, this is an id';
} else {
    echo 'No, this is not an id';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
No, this is not an id
```

**程序 2：**

## PHP

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div'));

// Create a id attribute
$attr = $element->setAttributeNode(
        new DOMAttr('id', 'mynewid'));

// Set that attribute as id
$element->setIDAttribute('id', true);

// Get the attribute
$getattr = $dom->getElementsByTagName('div')
        ->item(0)->getAttributeNode('id');

// Check if it is id or not
if($getattr->isId()) {
    echo 'Yes, this is an id';
} else {
    echo 'No, this is not an id';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
Yes, this is a id
```

**引用：**[https://www.php.net/manual/en/domattr.isid.php](https://www.php.net/manual/en/domattr.isid.php)
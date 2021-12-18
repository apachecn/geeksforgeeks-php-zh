# PHP|DOMElement setIdAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-setidattribute-function/](https://www.geeksforgeeks.org/php-domelement-setidattribute-function/)

**DOMElement：：setIdAttribute()函数**是 PHP 中的一个内置函数，用于将 name 指定的属性声明为 ID 类型。

**语法：**

```php
*void* DOMElement::setIdAttribute( *string* $name, *bool* $isId )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**它指定属性的名称。
*   **$isid：**它指定是否希望名称为 ID 类型。

**返回值：**此函数不返回任何内容。

**异常：**如果节点为只读，则此函数抛出 DOM_NO_MODIFICATION_ALLOWED_ERR；如果名称不是此元素的属性，则抛出 DOM_NOT_FOUND。

以下示例说明 PHP 中的**DOMElement：：setIdAttribute()函数**：

**示例 1：**

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div'));

// Create a id attribute to div
$attr = $element->setAttributeNode(new DOMAttr('id',
                                  'geeksforgeeks'));

// Set that attribute as id
$element->setIDAttribute('id', true);

echo $dom->saveXML();
?>
```

**输出：**按 Ctrl+U 查看 DOM。
![](img/01e92c64e120ceb11fcd0236d5a47e0f.png)

**示例 2：**

```php
<?php

// Create a new DOM Document
$dom = new DOMDocument('1.0', 'iso-8859-1');

// Enable validate on parse
$dom->validateOnParse = true;

// Create a div element
$element = $dom->appendChild(new DOMElement('div', 
                                 'GEEKSFORGEEKS'));

// Create a id attribute to div
$attr = $element->setAttributeNode(new DOMAttr('id', 
                                  'geeksforgeeks'));

// Set that attribute as id
$element->setIDAttribute('id', true);

// Get the text of element with id='geeksforgeeks'
// just to see if it works
$value = $dom->getElementById('geeksforgeeks')->textContent;

echo $value;
?>
```

发帖主题：Re：Колибри0.7.0

```php
GEEKSFORGEEKS
```

**引用：**[https://www.php.net/manual/en/domelement.setidattribute.php](https://www.php.net/manual/en/domelement.setidattribute.php)
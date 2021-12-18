# PHP|DOMElement getElementsByTagNameNS()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getelementsbytagnamens-function/](https://www.geeksforgeeks.org/php-domelement-getelementsbytagnamens-function/)

**DOMElement：：getElementsByTagNameNS()函数**是 PHP 中的一个内置函数，用于获取具有给定 localName 和 nampaceURI 的所有后代元素。

**语法：**

```php
*DOMNodeList* DOMElement::getElementsByTagNameNS( 
          *string* $namespaceURI, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI：**它指定命名空间 URI。
*   **$localName：**它指定本地名称。

**返回值：**此函数返回一个 DOMNodeList 值，其中包含所有匹配的元素，顺序与它们在此元素树的预序遍历中遇到的顺序相同。

下面给出的程序演示了 PHP 中的**DOMElement：：getElementsByTagNameNS()函数**：

**程序 1：**

```php
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <div xmlns:x=\"my_namespace\">
        <x:h1 x:style=\"color:red;\">
            Hello, this is my red heading.
        </x:h1>
        <x:h1 x:style=\"color:green;\">
            Hello, this is my green heading.
        </x:h1>
        <x:h1 x:style=\"color:blue;\">
            Hello, this is my blue heading.
        </x:h1>
    </div>
    <div xmlns:y=\"another_namespace\">
        <y:h1 y:style=\"color:red;\">
            Hello, this is my new red heading.
        </y:h1>
        <y:h1 y:style=\"color:green;\">
            Hello, this is my new green heading.
        </y:h1>
        <y:h1 y:style=\"color:blue;\">
            Hello, this is my new blue heading.
        </y:h1>
    </div>
</root>");

// Get the elements with h1 tag from
// specific namespace
$nodeList = $dom->getElementsByTagNameNS(
                    'my_namespace', 'h1');

foreach ($nodeList as $node) {
    echo $node->getAttribute('x:style') . '<br>';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
color:red;
color:green;
color:blue;
```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
    <div xmlns:x=\"my_namespace\">
        <x:p>HELLO.</x:p>
        <x:p>NEW.</x:p>
        <x:p>WORLD.</x:p>
    </div>
    <div xmlns:y=\"g4g_namespace\">
        <y:p>GEEKS</y:p>
        <y:p>FOR</y:p>
        <y:p>GEEKS</y:p>
    </div>
</root>");

// Get the elements
$nodeList = $dom->getElementsByTagNameNS(
                    'g4g_namespace', 'p');

foreach ($nodeList as $node) {
    echo $node->textContent . '<br>';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
GEEKS
FOR
GEEKS
```

**引用：**[https://www.php.net/manual/en/domelement.getelementsbytagnamens.php](https://www.php.net/manual/en/domelement.getelementsbytagnamens.php)
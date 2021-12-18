# PHP|DOMElement getElementsByTagName()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getelementsbytagname-function/](https://www.geeksforgeeks.org/php-domelement-getelementsbytagname-function/)

**DOMElement：：getElementsByTagName()函数**是 PHP 中的内置函数，用于按标记名获取元素。

**语法：**

```
*DOMNodeList* DOMElement::getElementsByTagName( *string* $name )
```

**参数：**此函数接受保存标记名的单个参数**$name**，或使用*获取所有标记。

**返回值：**此函数返回一个 DOMNodeList 值，该值包含具有给定标记名的所有后代元素，并按照它们在此元素树的预序遍历中遇到的顺序排列。

以下示例说明 PHP 中的**DOMElement：：getElementsByTagName()函数**：

**示例 1：**

## PHP

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
<body>
    <div>
    <h1 style=\"color:red;\"> Hello, this is my red heading. </h1>
    <h1 style=\"color:green;\"> Hello, this is my green heading. </h1>
    <h1 style=\"color:blue;\"> Hello, this is my blue heading. </h1>
    </div>
</body>
</root>");

// Save the XML
$nodeList = $dom->getElementsByTagName('h1');
foreach ($nodeList as $node) {
    // Get the attribute value of style
    echo $node->getAttribute('style') . '<br>';
}

?>
```

发帖主题：Re：Колибри0.7.0

```
color:red;
color:green;
color:blue;
```

**示例 2：**

## PHP

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<root>
<body>
    <div>

<p> Hello, this is my first paragraph. </p>

<p> Hello, this is my second paragraph. </p>

<p> Hello, this is my third paragraph. </p>

    </div>
</body>
</root>");

// Get the element by tagname
$nodeList = $dom->getElementsByTagName('p');

foreach ($nodeList as $node) {
    // Get the textContent
    echo $node->textContent . '<br>';
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Hello, this is my first paragraph.
Hello, this is my second paragraph.
Hello, this is my third paragraph.
```

**引用：**[https://www.php.net/manual/en/domelement.getelementsbytagname.php](https://www.php.net/manual/en/domelement.getelementsbytagname.php)
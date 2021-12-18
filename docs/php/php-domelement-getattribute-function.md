# PHP|DOMElement getAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-domelement-getattribute-function/](https://www.geeksforgeeks.org/php-domelement-getattribute-function/)

**DOMElement：：getAttribute()函数**是 PHP 中的一个内置函数，用于获取当前节点的名称属性值。

**语法：**

```
*string* DOMElement::getAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数返回包含属性值的字符串值。

下面给出的程序演示了 PHP 中的**DOMElement：：getAttribute()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<body>
    <strong attr=\"value\"> 22 </strong>
</body>");

// Get the strong element
$element = $dom->getElementsByTagName('strong');

// Get the attribute
$value = $element[0]->getAttribute('attr');
echo $value;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Load the XML
$dom->loadXML("<?xml version=\"1.0\"?>
<body>
    <div id=\"div1\"> DIV 1 </div>
    <div id=\"div2\"> DIV 2 </div>
    <div id=\"div3\"> DIV 3 </div>
</body>");

// Get all the div elements
$elements = $dom->getElementsByTagName('div');

// Get the id value of each element
echo "All the id values of divs are: <br>";
foreach ($elements as $element) {
    echo $element->getAttribute('id') . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domelement.getattribute.php](https://www.php.net/manual/en/domelement.getattribute.php)
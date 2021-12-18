# PHP|DOMDocument Valid()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-validate-function/](https://www.geeksforgeeks.org/php-domdocument-validate-function/)

**DOMDocument：：Valid()函数**是 PHP 中的一个内置函数，用于根据文档的 DTD(文档类型定义)验证文档。 DTD 定义 XML 文件要遵循的规则或结构，如果 XML 文档不遵循此格式，则此函数将返回 False。

**语法：**

```
*bool* DOMDocument::validate( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果文档遵循 DTD，则此函数返回 TRUE 或 FALSE。

下面的示例说明了 PHP 中的**DOMDocument：：Valid()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// Load the XML with DTD rule to have
// a root element with first, second,
// and third as its three children
$doc->loadXML("<?xml version=\"1.0\"?>
<!DOCTYPE root [
<!ELEMENT root (first, second, third)>
<!ELEMENT first (#PCDATA)>
<!ELEMENT second (#PCDATA)>
<!ELEMENT third (#PCDATA)>
]>

<!-- Create a XML following the DTD -->
<root>
<first>Hello</first>
<second>There</second>
<third>World</third>
</root>");

// Check if XML follows the DTD rule
if ($doc->validate()) {
    echo "This document is valid!\n";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// Load the XML
$doc->loadXML("<?xml version=\"1.0\"?>
<!DOCTYPE root [
<!ELEMENT root (one, two, three)>
<!ELEMENT one (#PCDATA)>
<!ELEMENT two (#PCDATA)>
<!ELEMENT three (#PCDATA)>
]>
<!-- Create a XML voilating the DTD -->

<root>
<one>Hello</one>
<two>World</two>
</root>");

if (!$doc->validate()) {
    echo "This document is not valid!";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.validate.php](https://www.php.net/manual/en/domdocument.validate.php)
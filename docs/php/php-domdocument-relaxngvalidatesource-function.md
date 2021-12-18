# PHP|DOMDocument 弛豫 NGValidateSource()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-relaxngvalidatesource-function/](https://www.geeksforgeeks.org/php-domdocument-relaxngvalidatesource-function/)

**DOMDocument：：relasNGValidateSource()函数**是 PHP 中的一个内置函数，用于使用字符串作为 RNG 模式对文档执行 RELANNG 验证。 *relasNGValify()*和*relacNGValidateSource()*之间的区别在于前者接受 RNG 模式文件名，而后者也可以接受字符串形式的 RNG 模式。

**语法：**

```
*bool* DOMDocument::relaxNGValidateSource( *string* $source )
```

**参数：**此函数接受保存 RNG 模式的单个参数**$source**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMDocument：：relasNGValidateSource()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// RNG schema
$RNG = "<element name=\"body\" 
    xmlns=\"http://relaxng.org/ns/structure/1.0\">
<zeroOrMore>
  <element name=\"div\">
    <element name=\"h1\">
      <text/>
    </element>
    <element name=\"h2\">
      <text/>
    </element>
  </element>
</zeroOrMore>
</element>";

// Load the XML
$doc->loadXML("<?xml version=\"1.0\"?>
<body>
  <div>
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
  </div>
  <div>
    <h1>Heading 3</h1>
    <h2>Heading 4</h2>
  </div>
</body>");

// Check if XML follows the relaxNG rule
if ($doc->relaxNGValidateSource($RNG)) {
    echo "This document is valid!\n";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// RNG schema
$RNG = "<element name=\"company\" 
    xmlns=\"http://relaxng.org/ns/structure/1.0\">
<zeroOrMore>
  <element name=\"employee\">
    <element name=\"name\">
      <text/>
    </element>
    <element name=\"salary\">
      <text/>
    </element>
  </element>
</zeroOrMore>
</element>";

// Load the XML
$doc->loadXML("<?xml version=\"1.0\"?>
<company>
  <employee>
    <name>John Smith</name>
    <salary>Web</salary>
  </employee>
  <employee>
    <!-- Do not add salary to voilate rule -->
    <name>John Doe</name>
  </employee>
</company>");

// Check if XML doesn't follows the relaxNG rule
if (!$doc->relaxNGValidateSource($RNG)) {
    echo "This document is not valid!\n";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.relaxngvalidatesource.php](https://www.php.net/manual/en/domdocument.relaxngvalidatesource.php)
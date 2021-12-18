# PHP|DOMXPath EVALUE()函数

> Original: [https://www.geeksforgeeks.org/php-domxpath-evaluate-function/](https://www.geeksforgeeks.org/php-domxpath-evaluate-function/)

**DOMXPath：：Evaluate()函数**是 PHP 中的一个内置函数，用于执行给定的 XPath 表达式，该表达式是为选择一组节点而定义的模式。
**语法：**和

```
*mixed* DOMXPath::evaluate( *string* $expression, 
          *DOMNode* $contextnode, *bool* $registerNodeNS )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expression：**它指定要执行的 XPath 表达式。
*   **$contextnode(可选)：**它指定执行相对 XPath 查询的上下文节点。 默认情况下，查询是相对于根元素的。
*   **$registerNodeNS(可选)：**它指定是否禁用上下文节点的自动注册。

**返回值：**如果成功，此函数返回 TRUE。
**异常：**此函数在出错时引发 DOMXPathException。
以下示例说明 PHP：
**中的**DOMXPath：：EVALUATE()函数**示例 1：**和

## PHP

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<bookstore>
<book>
  <title lang="en">GeeksforGeeks</title>
  <price>400</price>
</book>
<book>
  <title lang="en">Intro to XML</title>
  <price>300</price>
</book>
</bookstore>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Get the
$tbody = $document->
    getElementsByTagName('bookstore')->item(0);

// Query to get the number of titles with lang
// attribute "en"
$query = 'count(//title[@lang=\'en\'])';

// Evaluate the query
$entries = $xpath->evaluate($query, $tbody);
echo "Number of elements with lang = \"en\": $entries\n";
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Number of elements with lang = "en": 2
```

**示例 2：**和

## PHP

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<GeeksforGeeks>
  Keep Learning.
</GeeksforGeeks>
XML;

// Load the XML
$document->loadXML($xml);

// Create a new DOMXPath instance
$xpath = new DOMXPath($document);

// Get the
$tbody = $document->
getElementsByTagName('GeeksforGeeks')->item(0);

// Get the element with name GeeksforGeeks
$query = '//GeeksforGeeks';

// Evaluate the query
$entries = $xpath->evaluate($query, $tbody);
echo $entries[0]->nodeValue;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Keep Learning.
```

**引用：**[https://www.php.net/manual/en/domxpath.evaluate.php](https://www.php.net/manual/en/domxpath.evaluate.php)
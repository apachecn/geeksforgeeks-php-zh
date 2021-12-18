# PHP|DOMNode C14N()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-c14n-function/](https://www.geeksforgeeks.org/php-domnode-c14n-function/)

**DOMNode：：C14N()函数**是 PHP 中的一个内置函数，用于将节点转换为字符串。

**语法：**

```php
*string* DOMNode::C14N( *bool* $exclusive, 
*bool* $with_comments, *array* $xpath, *array* $ns_prefixes )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$EXCLUSIVE(可选)：**它指定是否只启用与所提供的 XPath 或名称空间前缀匹配的节点的独占解析。
*   **$WITH_COMMENTS(可选)：**它指定是否在输出中保留注释。
*   **$xpath(可选)：**它指定过滤节点的 xpath 数组。
*   **$ns_prefix(可选)：**它指定用于过滤节点的名称空间前缀数组。

**返回值：**此函数以字符串形式返回规范化节点，失败时返回 False。

下面的示例说明了 PHP 中的**DOMNode：：C14N()函数**：

**示例 1：**

```php
<?php

// Create a DOMDocument
$doc = new DOMDocument();

// Load XML
$doc->loadXML('<html></html>');

// Create an heading element on 
// DOMDocument object
$h1 = $doc->createElement('h1');

// Append the child
$doc->documentElement->appendChild($h1);

// Get the data without comments
$stringdata = $doc->C14N();
echo $stringdata;
?>
```

发帖主题：Re：Колибри0.7.0

```php
<html><h1></h1></html>
```

**示例 2：**

```php
<?php
// Create a DOMDocument
$doc = new DOMDocument();

// Load XML
$doc->loadXML('<html><!-- This is a comment --></html>');

// Create an heading element on DOMDocument object
$h1 = $doc->createElement('h1');

// Append the child
$doc->documentElement->appendChild($h1);

// Get the data with comments
$stringdata = $doc->C14N(false, true);
echo 'With Comments: <br>';
echo htmlentities($stringdata);

// Get the data without comments
$stringdata = $doc->C14N(false, false);
echo '<br>Without Comments: <br>';
echo htmlentities($stringdata);
?>
```

发帖主题：Re：Колибри0.7.0

```php
With Comments: 
<html><!-- This is a comment --><h1></h1></html>
Without Comments: 
<html><h1></h1></html>
```

**引用：**[https://www.php.net/manual/en/domnode.c14n.php](https://www.php.net/manual/en/domnode.c14n.php)
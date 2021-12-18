# PHP|DOMNode C14NFile()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-c14nfile-function/](https://www.geeksforgeeks.org/php-domnode-c14nfile-function/)

**DOMNode：：C14NFile()函数**是 PHP 中的一个内置函数，用于将节点规范化为文件。

**语法：**

```
*int* DOMNode::C14NFile( *string* $uri, *bool* $exclusive, 
*bool* $with_comments, *array* $xpath, *array* $ns_prefixes )
```

**参数：**此函数接受五个参数，如上所述，如下所述：

*   **$uri (optional):** it specifies the path to write the output.
*   **$EXCLUSIVE (optional):** it specifies whether exclusive resolution is enabled for only nodes that match the supplied XPath or namespace prefix.
*   **$WITH_COMMENTS (optional):** it specifies whether to retain comments in the output.
*   **$xpath (optional):** it specifies the xpath array by which the nodes are filtered.
*   **$ns_prefix (optional):** it specifies the namespace prefix array used to filter nodes.

**返回值：**此函数返回失败时写入的字节数或 FALSE

以下示例说明 PHP 中的**DOMNode：：C14NFile()函数**：

**示例 1：**在此示例中，我们将字符串形式的 DOM 内容保存到不带注释的文件

```
<?php

// Create a DOMDocument
$doc = new DOMDocument();

// Load XML
$doc->loadXML('<html></html>');

// Create an heading element on DOMDocument object
$h1 = $doc->createElement('h1');

// Append the child
$doc->documentElement->appendChild($h1);

// Save the data without comments
$stringdata = $doc->C14NFile('new.txt');
?>
```

**输出：**这将创建一个具有以下文本内容

```
<html><h1></h1></html>
```

的新.txt 文件

**示例 2：**在本例中，我们将字符串形式的 DOM 内容保存到一个带有注释的文件中。

```
<?php

// Create a DOMDocument
$doc = new DOMDocument();

// Load XML
$doc->loadXML('<html><!-- This is a comment --></html>');

// Create an heading element on DOMDocument object
$h1 = $doc->createElement('h1');

// Append the child
$doc->documentElement->appendChild($h1);

// Save the data with comments
$stringdata = $doc->C14NFile('new.txt', false, true);
?>
```

**输出：**这将创建一个具有以下文本内容

```
<html><!-- This is a comment --><h1></h1></html>
```

的新.txt 文件

**引用：**[https://www.php.net/manual/en/domnode.c14nfile.php](https://www.php.net/manual/en/domnode.c14nfile.php)
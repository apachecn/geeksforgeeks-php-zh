# PHP|DOMNode hasChildNodes()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-haschildnodes-function/](https://www.geeksforgeeks.org/php-domnode-haschildnodes-function/)

**DOMNode：：hasChildNodes()函数**是 PHP 中的一个内置函数，用于检查节点是否有子节点。

**语法：**

```php
*bool* DOMNode::hasChildNodes( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMNode：：hasChildNodes()函数**：

**程序 1：**

```php
<?php
// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element
$element = $dom->createElement('p', 'GeeksforGeeks!');

// Append the child
$dom->appendChild($element);

// Check if child nodes are there
if ($dom->hasChildNodes()) {
    echo "Yes, child nodes are there.";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
// Create a new DOMDocument instance and keep it empty
$dom = new DOMDocument();

// Check if child nodes are not there
if (!$dom->hasChildNodes()) {
    echo "No, child nodes are not there.";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.haschildnodes.php](https://www.php.net/manual/en/domnode.haschildnodes.php)
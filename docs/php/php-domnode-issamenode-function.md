# PHP|DOMNode isSameNode()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-issamenode-function/](https://www.geeksforgeeks.org/php-domnode-issamenode-function/)

**DOMNode：：isSameNode()函数**是 PHP 中的一个内置函数，用于指示两个节点是否为同一节点。

**语法：**

```
*bool* DOMNode::isSameNode( *DOMNode* $node )
```

**参数：**此函数接受单个参数**$node**，该参数保存要比较的节点。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMNode：：isSameNode()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element with a namespace
$p_element = $dom->createElementNS(
      'my_namespace', 'p', 'GeeksforGeeks');

// Append the child to DOMDocument
$dom->appendChild($p_element);

// Check if the node is same
$isSameNode = $dom->isSameNode($dom);

// Check if the namespace is default or not
if($isSameNode) {
    echo 'Yes, $dom is same to itself.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element with a namespace
$p_element = $dom->createElementNS(
      'my_namespace', 'p', 'GeeksforGeeks');

// Append the child to DOMDocument
$dom->appendChild($p_element);

// Create another new DOMDocument instance
$dom2 = new DOMDocument();

// Check if nodes are same
$isSameNode = $dom->isSameNode($dom2);

// Check if the namespace is default or not
if(!$isSameNode) {
    echo 'No, $dom and $dom2 are different.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.issamenode.php](https://www.php.net/manual/en/domnode.issamenode.php)
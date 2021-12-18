# PHP|DOMNode isDefaultNamespace()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-isdefaultnamespace-function/](https://www.geeksforgeeks.org/php-domnode-isdefaultnamespace-function/)

**DOMNode：：isDefaultNamespace()函数**是 PHP 中的内置函数，用于检查指定的名称空间 URI 是否为默认名称空间。

**语法：**

```php
*bool* DOMNode::isDefaultNamespace( *string* $namespaceURI )
```

**参数：**此函数接受单个参数**$nampaceURI**，该参数保存命名空间 URI。

**返回值：**如果 nampaceURI 是默认命名空间，则此函数返回 TRUE，否则返回 FALSE。

以下示例说明 PHP 中的**DOMNode：：isDefaultNamespace()函数**：

**示例 1：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element with a namespace
$p_element = $dom->createElementNS(
    'my_namespace', 'p', 'GeeksforGeeks');

// Append the child to DOMDocument
$dom->appendChild($p_element);

// Check if the namespace is default or not
if($dom->isDefaultNamespace('my_namespace')) {
    echo 'Yes, my_namespace is the default namespace.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new DOMDocument
$dom = new DOMDocument();

// Create a paragraph element with a namespace
$p_element = $dom->createElementNS(
    'my_namespace', 'p', 'GeeksforGeeks');

// Append the child to DOMDocument
$dom->appendChild($p_element);

// Check if the namespace is default or not
if(!$dom->isDefaultNamespace('some_other_namespace'))
{
    echo 'No, some_other_namespace is not'
                         . ' default namespace.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.isdefaultnamespace.php](https://www.php.net/manual/en/domnode.isdefaultnamespace.php)
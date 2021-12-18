# PHP|DOMNode lookupNamespaceUri()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-lookupnamespaceuri-function/](https://www.geeksforgeeks.org/php-domnode-lookupnamespaceuri-function/)

**DOMNode：：lookupNamespaceUri()函数**是 PHP 中的一个内置函数，用于根据前缀获取节点的命名空间 URI。

**语法：**

```php
*string* DOMNode::lookupNamespaceUri( *string* $prefix )
```

**参数：**此函数接受包含前缀的单个参数**$prefix**。

**返回值：**此函数返回节点的命名空间 URI。

以下示例说明 PHP 中的**DOMNode：：lookupNamespaceUri()函数**：

**示例 1：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Create a XML variable with no namespace
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <h1>GeeksforGeeks</h1>
</root>
XML;

// Load the XML
$document->loadXML($xml);

// Get the default namespace URI
$uri = $document->documentElement->lookupnamespaceURI(null);
echo $uri;
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Load the XML with a namespace with prefix x
$document->loadXML("<?xml version=\"1.0\"?>
    <div xmlns:x=\"my_namespace\">
        <x:h1 x:style=\"color:red;\"> GeeksforGeeks </x:h1>
    </div>
");

// Get the URI with prefix x
$uri = $document->documentElement->lookupnamespaceURI('x');
echo $uri;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.lookupnamespaceuri.php](https://www.php.net/manual/en/domnode.lookupnamespaceuri.php)
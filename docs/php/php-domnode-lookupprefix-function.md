# PHP|DOMNode lookupPrefix()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-lookupprefix-function/](https://www.geeksforgeeks.org/php-domnode-lookupprefix-function/)

**DOMNode：：lookupPrefix()函数**是 PHP 中的一个内置函数，用于根据名称空间 URI 获取节点的名称空间前缀。
**语法：**和

```
*string* DOMNode::lookupPrefix( *string* $namespaceURI )
```

**参数：**此函数接受单个参数**$nampaceURI**，该参数保存命名空间 URI。
**返回值：**此函数返回命名空间的前缀。
以下示例说明 PHP：
**示例 1：**和
中的**DOMNode：：lookupPrefix()函数**

## PHP

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Load the XML with no namespace
$document->loadXML("<?xml version=\"1.0\"?>
    <div >
        <h1> GeeksforGeeks </h1>
    </div>
");

// Get the prefix with namespace URI "my_namespace"
$prefix = $document->documentElement->
           lookupPrefix("my_nsamespace");
echo $prefix;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
// Empty string as there is no such namespace
```

**示例 2：**和

## PHP

```
<?php

// Create a new DOMDocument instance
$document = new DOMDocument();

// Load the XML with a namespace with prefix x
$document->loadXML("<?xml version=\"1.0\"?>
    <div xmlns:x=\"my_namespace\">
        <x:h1 x:style=\"color:red;\">
         GeeksforGeeks
        </x:h1>
    </div>
");

// Get the prefix with namespace URI "my_namespace"
$prefix = $document->documentElement->
          lookupPrefix('my_namespace');
echo $prefix;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
x
```

**引用：**[https://www.php.net/manual/en/domnode.lookupprefix.php](https://www.php.net/manual/en/domnode.lookupprefix.php)
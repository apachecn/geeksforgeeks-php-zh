# PHP|DOMNode getNodePath()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-getnodepath-function/](https://www.geeksforgeeks.org/php-domnode-getnodepath-function/)

**DOMNode：：getNodePath()函数**是 PHP 中的一个内置函数，用于获取节点的 XPath 位置路径。

**语法：**

```
*string* DOMNode::getNodePath( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 XPath 的字符串，如果出现错误，则返回 NULL。

以下示例说明 PHP 中的**DOMNode：：getNodePath()函数**：

**示例 1：**

```
<?php

// Create a new DOMDocument instance
$dom = new DOMDocument;

// Load the XML
$dom->loadXML('
<root>
    <h1>GeeksforGeeks</h1>
</root>
');

// Print XPath of the element
echo $dom->getElementsByTagName('h1')
    ->item(0)->getNodePath();
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a new DOMDocument instance
$dom = new DOMDocument;

// Load the XML
$dom->loadXML('
<root>
    <h1>Geeks</h1>
    <div>
        <h1>For</h1>
    </div>
    <h1>Geeks</h1>
</root>
');

// Print XPath of the element
for ($i = 0; $i < 3; $i++) {

    // Print where the line where the 'node' 
    // element was defined in
    echo $i+1 . ') The h1 tag\'s Xpath is: ' 
        . $dom->getElementsByTagName('h1')
        ->item($i)->getNodePath() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.getnodepath.php](https://www.php.net/manual/en/domnode.getnodepath.php)
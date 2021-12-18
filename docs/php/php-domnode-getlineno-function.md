# PHP|DOMNode getLineNo()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-getlineno-function/](https://www.geeksforgeeks.org/php-domnode-getlineno-function/)

**DOMNode：：getLineNo()函数**是 PHP 中的一个内置函数，用于获取定义节点的行号。

**语法：**

```php
*DOMNode* DOMNode::getLineNo( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回在中定义节点的行号。

下面给出的程序说明了 PHP：
**程序 1：**中的**DOMNode：：getLineNo()函数**

```php
<?php
// Create a XML variable
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <h1>GeeksforGeeks</h1>
</root>
XML;

// Create a new DOMDocument instance
$dom = new DOMDocument;

// Load the XML
$dom->loadXML($xml);

// Print where the line where the 'node' element was defined in
echo 'The <node> tag is defined on line ' . $dom->getElementsByTagName('h1')->item(0)->getLineNo();
?>
```

发帖主题：Re：Колибри0.7.0

```php
The tag is defined on line 3
```

**程序 2：**

```php
<?php
// Create a XML variable
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <h1>Geeks</h1>
    <h1>For</h1>
    <h1>Geeks</h1>
</root>
XML;

// Create a new DOMDocument instance
$dom = new DOMDocument();

// Load the XML
$dom->loadXML($xml);

for ($i = 0; $i < 3; $i++) {
    // Print where the line where the 'node' element was defined in
    echo $i . ') The h1 tag is defined on line ' . $dom->getElementsByTagName('h1')->item($i)->getLineNo() . "<br>";

}
?>
```

发帖主题：Re：Колибри0.7.0

```php
0) The h1 tag is defined on line 3
1) The h1 tag is defined on line 4
2) The h1 tag is defined on line 5
```

**引用：**[https://www.php.net/manual/en/domnode.getlineno.php](https://www.php.net/manual/en/domnode.getlineno.php)
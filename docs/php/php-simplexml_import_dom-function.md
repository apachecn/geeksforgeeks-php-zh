# PHP|simplexml_import_dom()函数

> Original: [https://www.geeksforgeeks.org/php-simplexml_import_dom-function/](https://www.geeksforgeeks.org/php-simplexml_import_dom-function/)

函数**simplexml_import_dom()**位于 PHP 的内置函数中，该函数用于获取 DOM 文档的节点并将其转换为 SimpleXML 节点。

**语法：**

```php
*SimpleXMLElement* simplexml_import_dom( $node, $class_name = "SimpleXMLElement" )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$node:** this parameter saves the DOM element node.
*   **$CLASS_NAME:** saves the optional parameters for the class name. If this parameter is used, the simplexml_import_dom () function returns the object of the specified class. This class should extend the SimpleXMLElement class.

**返回值：**此函数成功时返回 SimpleXMLElement，失败时返回 False。

下面的程序演示了 PHP 中的 simplexml_import_dom()函数：

**程序：**

```php
<?php

// Create an instance of DOMDocument
$dom = new DOMDocument;

// Load XML document
$dom -> loadXML('<organization>
        <name>GeeksforGeeks</name>
        <address>Noida India</address>
        <contact>
            <email>abc@geeksforgeeks.org</email>
            <mobile>+91-987654321</mobile>
        </contact>
    </organization>'
);

// Use simplexml_import_dom() function to get a
// SimpleXMLElement object from a DOM node
$doc = simplexml_import_dom($dom);

// Display the content of XML document
var_dump($doc->contact[0]->email);
var_dump($doc->contact[0]->mobile);

?>
```

**输出：**

```php
object(SimpleXMLElement)#3 (1) {
  [0]=>
  string(21) "abc@geeksforgeeks.org"
}
object(SimpleXMLElement)#3 (1) {
  [0]=>
  string(13) "+91-987654321"
}

```

**引用：**[https://www.php.net/manual/en/function.simplexml-import-dom.php](https://www.php.net/manual/en/function.simplexml-import-dom.php)
# PHP|SimpleXMLIterator getChildren()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-getchildren-function/](https://www.geeksforgeeks.org/php-simplexmliterator-getchildren-function/)

**SimpleXMLIterator：：getChildren()函数**是 PHP 中的内置函数，用于返回包含当前元素的子元素的 SimpleXMLIterator 对象。

**语法：**

```
*SimpleXMLIterator* SimpleXMLIterator::getChildren( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含当前元素的子元素的 SimpleXMLIterator 对象。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：getChildren()函数：

**程序：**

```
<?php

// Store the xml element to variable
$xml = <<<XML
    <organization>
        <name>GeeksforGeeks</name>
        <address>Noida India</address>
        <contact>
            <email>abc@geeksforgeeks.org</email>
            <mobile>+91-987654321</mobile>
        </contact>
    </organization>
XML;

$xmlIt = new SimpleXMLIterator($xml);

// Loop starts from first element of xml and 
// run upto when elements are not valid
for( $xmlIt->rewind(); $xmlIt->valid(); $xmlIt->next() ) {

    foreach($xmlIt->getChildren() as $element => $content) {
        echo "The content of '$element' element is '$content'" . "\n";
    }
}

?>
```

**输出：**

```
The content of 'email' element is 'abc@geeksforgeeks.org'
The content of 'mobile' element is '+91-987654321'

```

**引用：**[https://www.php.net/manual/en/simplexmliterator.getchildren.php](https://www.php.net/manual/en/simplexmliterator.getchildren.php)
# PHP|SimpleXMLIterator hasChildren()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-haschildren-function/](https://www.geeksforgeeks.org/php-simplexmliterator-haschildren-function/)

**SimpleXMLIterator：：hasChildren()函数**是 PHP 中的一个内置函数，用于检查当前 SimpleXMLIterator 元素是否有子元素。

**语法：**

```php
*bool* SimpleXMLIterator::hasChildren( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果当前元素有子元素，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：hasChildren()函数：

**程序：**

```php
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

    if($xmlIt->hasChildren()) {
        print_r($xmlIt->current());
    }
}

?>
```

**输出：**

```php
SimpleXMLIterator Object
(
    [email] => abc@geeksforgeeks.org
    [mobile] => +91-987654321
)

```

**引用：**[https://www.php.net/manual/en/simplexmliterator.haschildren.php](https://www.php.net/manual/en/simplexmliterator.haschildren.php)
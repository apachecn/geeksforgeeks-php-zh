# PHP|SimpleXMLIterator key()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-key-function/](https://www.geeksforgeeks.org/php-simplexmliterator-key-function/)

**SimpleXMLIterator：：key()函数**是 PHP 中的内置函数，用于返回当前元素的键。

**语法：**

```php
*mixed* SimpleXMLIterator::key( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回元素 SimpleXMLIterator 对象的 XML 标记名，失败时返回 False。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：key()函数：

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

    var_dump($xmlIt->key());
}

?>
```

**输出：**

```php
string(4) "name"
string(7) "address"
string(7) "contact"

```

**引用：**[https://www.php.net/manual/en/simplexmliterator.key.php](https://www.php.net/manual/en/simplexmliterator.key.php)
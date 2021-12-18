# PHP|SimpleXMLIterator 倒带()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-rewind-function/](https://www.geeksforgeeks.org/php-simplexmliterator-rewind-function/)

**SimpleXMLIterator：：Rewind()函数**是 PHP 中的一个内置函数，用于将 SimpleXMLIterator 倒回到第一个元素。

**语法：**

```php
*void* SimpleXMLIterator::rewind( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：Rewind()函数：

**程序 1：**

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

// Use rewind() function to rewind
// to the first element
$xmlIt->rewind();

// Use next() function to move to the
// next element
$xmlIt->next();
$xmlIt->next();

// Display result
var_dump($xmlIt->current());

?>
```

**输出：**

```php
object(SimpleXMLIterator)#2 (2) {
  ["email"]=>
  string(21) "abc@geeksforgeeks.org"
  ["mobile"]=>
  string(13) "+91-987654321"
}

```

**程序 2：**

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

**引用：**[https://www.php.net/manual/en/simplexmliterator.rewind.php](https://www.php.net/manual/en/simplexmliterator.rewind.php)
# PHP|SimpleXMLIterator Next()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-next-function/](https://www.geeksforgeeks.org/php-simplexmliterator-next-function/)

**SimpleXMLIterator：：Next()函数**是 PHP 中的一个内置函数，用于将 SimpleXMLIterator 元素移动到下一个元素。

**语法：**

```php
*void* SimpleXMLIterator::next( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：Next()函数：

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

// Use rewind() function to rewind
// to the first element
$xmlIt->rewind();

// Use next() function to move
// to the next element
$xmlIt->next();
$xmlIt->next();

// Display the current element
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

**引用：**[https://www.php.net/manual/en/simplexmliterator.next.php](https://www.php.net/manual/en/simplexmliterator.next.php)
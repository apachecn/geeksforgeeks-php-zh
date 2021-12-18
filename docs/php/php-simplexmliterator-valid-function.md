# PHP|SimpleXMLIterator Valid()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-valid-function/](https://www.geeksforgeeks.org/php-simplexmliterator-valid-function/)

**SimpleXMLIterator：：Valid()函数**是 PHP 中的内置函数，用于检查当前元素是否有效。

**语法：**

```php
*bool* SimpleXMLIterator::valid( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果当前元素有效，则此函数返回 TRUE，如果失败，则返回 FALSE。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：Valid()函数：

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

// Display the result
var_dump($xmlIt->valid());

// Use next() function to move
// the next element
$xmlIt->next();
$xmlIt->next();
$xmlIt->next();

// Display the result
var_dump($xmlIt->valid());

?>
```

**输出：**

```php
bool(true)
bool(false)

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

**引用：**[https://www.php.net/manual/en/simplexmliterator.valid.php](https://www.php.net/manual/en/simplexmliterator.valid.php)
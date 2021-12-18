# PHP|SimpleXMLIterator Current()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmliterator-current-function/](https://www.geeksforgeeks.org/php-simplexmliterator-current-function/)

**SimpleXMLIterator：：Current()函数**是 PHP 中的内置函数，用于将当前元素作为 SimpleXMLIterator 对象或 NULL 返回。

**语法：**

```php
*mixed* SimpleXMLIterator::current( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时作为 SimpleXMLIterator 对象返回当前元素，失败时返回 NULL。

下面的程序演示了 PHP 中的 SimpleXMLIterator：：Current()函数：

**程序 1：**

```php
<?php

// Create new SimpleXMLIterator object
$xmlIt = new SimpleXMLIterator(
    '<organization>
        <name>GeeksforGeeks</name>
        <address>Noida India</address>
        <email>abc@geeksforgeeks.org</email>
    </organization>'
);

// Display the current string
var_dump($xmlIt->current());

// Use rewind() function to first element
$xmlIt->rewind();

// Display the current string
var_dump($xmlIt->current());

?>
```

**输出：**

```php
NULL
object(SimpleXMLIterator)#2 (1) {
  [0]=>
  string(13) "GeeksforGeeks"
}

```

**程序 2：**

```php
<?php

// Create new SimpleXMLIterator object
$xmlIt = new SimpleXMLIterator(
    '<organization>
        <name>GeeksforGeeks</name>
        <address>Noida India</address>
        <email>abc@geeksforgeeks.org</email>
    </organization>'
);

// Use rewind() function to first element
$xmlIt->rewind();

// Use next() function to get
// the next element
$xmlIt->next();

// Display the current string
var_dump($xmlIt->current());

?>
```

**输出：**

```php
object(SimpleXMLIterator)#2 (1) {
  [0]=>
  string(11) "Noida India"
}

```

**引用：**[https://www.php.net/manual/en/simplexmliterator.current.php](https://www.php.net/manual/en/simplexmliterator.current.php)
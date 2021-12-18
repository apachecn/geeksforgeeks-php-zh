# PHP | ArrayIterator serialize()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-serialize-function/](https://www.geeksforgeeks.org/php-arrayiterator-serialize-function/)

**数组迭代器::serialize()函数**是 PHP 中的一个内置函数，用于序列化数组迭代器。

**语法:**

```php
*string* ArrayIterator::serialize( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回序列化数组运算符。

下面的程序说明了 PHP 中的 ArrayIterator::serialize()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

// Serialize the element
$serialize = $arrItr->serialize(); 

// Display the output
var_dump($serialize);

?>
```

**输出:**

> 字符串(81)“x:I:0；a:5:{ I:0；s:1:“G”；一:1；s:1:“e”；一:2；s:1:“e”；一:3；s:1:“k”；一:4；s:1:“s”；};m:a:0:{}"

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => "Geeks",
        "b" => "for",
        "c" => "Geeks"
    )
);

// Append some elements
$arrItr->append("Computer"); 
$arrItr->append("Science"); 
$arrItr->append("Portal"); 

// Serialize the element
$serialize = $arrItr->serialize(); 

// Display the output
var_dump($serialize);

?>
```

**输出:**

> 字符串(133)“x:I:0；a:6:{ s:1:" a "；s:5:“极客”；s:1:“b”；s:3:“用于”；s:1:“c”；s:5:“极客”；I:0；s:8:“计算机”；一:1；s:7:“科学”；一:2；s:6:“门户”；};m:a:0:{}"

**参考:**T2】https://www.php.net/manual/en/arrayiterator.serialize.php
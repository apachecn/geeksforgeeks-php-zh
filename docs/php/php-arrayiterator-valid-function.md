# PHP | ArrayIterator 有效()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayiterator-valid-function/](https://www.geeksforgeeks.org/php-arrayiterator-valid-function/)

**ArrayIterator::valid()函数**是 PHP 中的一个内置函数，用来检查一个数组是否包含更多的条目。

**语法:**

```php
*bool* ArrayIterator::valid( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**如果迭代器有效，该函数返回真，否则返回假。

下面的程序说明了 PHP 中的 ArrayIterator::valid()函数:
**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

while ($arrItr->valid()) {
    echo "ArrayIterator Key: " . $arrItr->key() .
    "  ArrayIterator Value: " . $arrItr->current() . "\n";

    $arrItr->next();
}

?>
```

**Output:**

```php
ArrayIterator Key: 0  ArrayIterator Value: G
ArrayIterator Key: 1  ArrayIterator Value: e
ArrayIterator Key: 2  ArrayIterator Value: e
ArrayIterator Key: 3  ArrayIterator Value: k
ArrayIterator Key: 4  ArrayIterator Value: s

```

**程序 2:**

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

// Using rewind function 
$arrItr->rewind(); 

while($arrItr->valid()) { 
    var_dump($arrItr->current()); 

    // Moving to next element 
    $arrItr->next(); 
} 

?>
```

**Output:**

```php
string(5) "Geeks"
string(3) "for"
string(5) "Geeks"

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.valid.php
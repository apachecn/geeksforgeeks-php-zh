# PHP | ArrayIterator ksort()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-k sort-function/](https://www.geeksforgeeks.org/php-arrayiterator-ksort-function/)

**ArrayIterator::ksort()函数**是 PHP 中的一个内置函数，用于按键对数组元素进行排序。

**语法:**

```php
*void* ArrayIterator::ksort( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::ksort()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        5 => 'G',
        4 => 'e',
        3 => 'e',
        2 => 'k',
        1 => 's', 
        6 => 'f',
        8 => 'o',
        7 => 'r'
    )
);

// Sort the array element by key
$arrItr->ksort();

// Display the element
while($arrItr->valid()) {
    echo $arrItr->current() . " ";
    $arrItr->next();
}

?>
```

**输出:**

```php
s k e e G f r o

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => "Geeks",
        "c" => "for",
        "b" => "Geeks"
    )
);

// Append the element into array
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Sort the array element by key
$arrItr->ksort();

// Display the result
foreach($arrItr as $element) {
    echo "key: " . $arrItr->key() . "  Value: "
            . $arrItr->current() . "\n";
}

?>
```

**输出:**

```php
key: a  Value: Geeks
key: b  Value: Geeks
key: c  Value: for
key: 0  Value: Computer
key: 1  Value: Science
key: 2  Value: Portal

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.ksort.php
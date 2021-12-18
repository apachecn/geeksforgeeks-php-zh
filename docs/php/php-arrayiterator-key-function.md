# PHP | ArrayIterator 键()功能

> 原文:[https://www . geesforgeks . org/PHP-arrayiterator-key-function/](https://www.geeksforgeeks.org/php-arrayiterator-key-function/)

**ArrayIterator::key()函数**是 PHP 中的一个内置函数，返回数组元素的当前键。

**语法:**

```php
*mixed* ArrayIterator::key( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**此函数返回当前数组键。

下面的程序说明了 PHP 中的 ArrayIterator::key()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Loop to display the array iterator key
foreach($arrItr as $element) {
    echo $arrItr->key() . "\n";
}

?>
```

**输出:**

```php
0
1
2
3
4
5
6
7

```

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

// Append the element into array iterator
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Display the key and its value of
// array iterator
foreach($arrItr as $element) {
    echo "key: " . $arrItr->key() . "  Value: "
            . $arrItr->current() . "\n";
}

?>
```

**输出:**

```php
key: a  Value: Geeks
key: b  Value: for
key: c  Value: Geeks
key: 0  Value: Computer
key: 1  Value: Science
key: 2  Value: Portal

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.key.php
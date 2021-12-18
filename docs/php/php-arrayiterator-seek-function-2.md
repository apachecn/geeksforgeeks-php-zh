# PHP | ArrayIterator seek()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayiterator-seek-function-2/](https://www.geeksforgeeks.org/php-arrayiterator-seek-function-2/)

**ArrayIterator::seek()函数**是 PHP 中的一个内置函数，用于查找数组迭代器的位置。

**语法:**

```php
*void* ArrayIterator::seek( *int* $position )
```

**参数:**该功能接受单个参数 **$position** ，该参数持有要寻找的位置。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::seek()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => 4,
        "b" => 2,
        "g" => 8,
        "d" => 6,
        "e" => 1,
        "f" => 9
    )
);

// Seek the position
$arrItr->seek(5);

// Display the element
echo $arrItr->current();

?>
```

**输出:**

```php
9

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "b" => "for",
        "a" => "Geeks",
        "e" => "Science",
        "c" => "Geeks",
        "f" => "Portal",
        "d" => "Computer"
    )
);

// Check the validity of ArrayIterator
if($arrItr->valid()) {

    // Seek the position
    $arrItr->seek(3);

    // Display the element
    echo $arrItr->current();
}

?>
```

**输出:**

```php
Geeks

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.seek.php
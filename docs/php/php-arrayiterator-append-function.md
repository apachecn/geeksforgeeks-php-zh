# PHP | ArrayIterator append()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-append-function/](https://www.geeksforgeeks.org/php-arrayiterator-append-function/)

**ArrayIterator::append()函数**是 PHP 中的一个内置函数，用于将元素追加到数组迭代器中。

**语法:**

```php
*void* ArrayIterator::append( *mixed* $value )
```

**参数:**该函数接受保存需要追加的值的单个参数**$值**。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::append()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

// Append the element into array iterator
$arrItr->append("123");

// Display the elements
while($arrItr->valid()) {
    echo $arrItr->current();
    $arrItr->next();
}

?>
```

**输出:**

```php
Geeks123

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

// Append the array element
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Display the elements
foreach ($arrItr as $key => $val) {
    echo $key . " => " . $val . "\n";
}

?>
```

**输出:**

```php
a => Geeks
b => for
c => Geeks
0 => Computer
1 => Science
2 => Portal

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.append.php
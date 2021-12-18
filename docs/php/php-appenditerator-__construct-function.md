# PHP | AppendIterator _ _ construct()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-_ _ construct-function/](https://www.geeksforgeeks.org/php-appenditerator-__construct-function/)

**AppendIterator::__construct()函数**是 PHP 中的一个内置函数，用于构造一个 AppendIterator。

**语法:**

```php
*public* AppendIterator::__construct( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 AppendIterator::__construct()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));
$arr2 = new ArrayIterator(array('f', 'o', 'r'));
$arr3 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);
$itr->append($arr3);

// Display the result
foreach ($itr as $key => $val) {
    echo $key . " => " . $val . PHP_EOL;
}

?>
```

**输出:**

```php
0 => G
1 => e
2 => e
3 => k
4 => s
0 => f
1 => o
2 => r
0 => G
1 => e
2 => e
3 => k
4 => s

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array("Geeks", "for", "Geeks"));
$arr2 = new ArrayIterator(array("Computer", "Science", "Portal"));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);

// Display the result
foreach ($itr as $key => $val) {
    echo $key . " => " . $val . PHP_EOL;
}

?>
```

**输出:**

```php
0 => Geeks
1 => for
2 => Geeks
0 => Computer
1 => Science
2 => Portal

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.construct.php
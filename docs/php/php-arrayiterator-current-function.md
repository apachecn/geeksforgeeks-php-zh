# PHP | ArrayIterator current()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-current-function/](https://www.geeksforgeeks.org/php-arrayiterator-current-function/)

**ArrayIterator::current()函数**是 PHP 中的一个内置函数，用来返回数组迭代器的当前元素。

**语法:**

```php
*mixed* ArrayIterator::current( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回数组的当前元素。

下面的程序说明了 PHP 中的 ArrayIterator::current()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Loop to display the element
while($arrItr->valid()) {
    echo $arrItr->current();
    $arrItr->next();
}

?>
```

**输出:**

```php
Geeksfor

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks")
);

// Loop to display the element
foreach($arrItr as $element) {
    echo $arrItr->current() . "\n";
}

?>
```

**输出:**

```php
Geeks
for
Geeks

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.current.php
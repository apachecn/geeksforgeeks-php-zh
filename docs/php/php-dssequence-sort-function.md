# PHP|ds\Sequence Sort()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-sort-function/](https://www.geeksforgeeks.org/php-dssequence-sort-function/)

**Ds\Sequence：：Sort()**函数是 PHP 中的一个内置函数，用于对同一位置的 Sequence 元素进行排序。

**语法：**

```php
*void* abstract public Ds\Sequence::sort ([ callable $comparator ] )

```

**参数：**此函数接受单个参数*$compator*，该参数用于保存比较函数。 COMPARY 函数返回小于、大于或等于零的整数值。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Sequence：：Sort()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([2, 4, 1, 9, 6, 5, 12, 9]);

// Use sort() function to sort
// the sequence element
$seq->sort();

print_r($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([2, 4, 1, 9, 6, 5, 12, 9]);

// Use sort() function to sort
// the sequence element
$seq->sort(function($x, $y) {
    return $y <=> $x;
});

print_r($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.sort.php](http://php.net/manual/en/ds-sequence.sort.php)
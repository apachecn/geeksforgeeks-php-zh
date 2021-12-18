# PHP|Ds\Vector Sort()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-sort-function/](https://www.geeksforgeeks.org/php-dsvector-sort-function/)

**ds\Vector：：Sort()**函数是 PHP 中的一个内置函数，用于就地对向量的元素进行排序。 这将按升序排列向量元素。

**语法：**

```php
*void* public Ds\Vector::sort( $comparator )

```

**参数：**此函数接受单个参数*$compator*，该参数用于保存排序函数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Vector：：Sort()**函数：

**程序 1：**

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector([6, 5, 4, 3, 2, 1]);

echo("Original vector\n");

// Display the vector elements
print_r($vect);

// Use sort() function to sort
// the vector elements
$vect->sort();

echo("\nSorted elements\n");

// Display the sorted vector 
// elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector([3, 6, 1, 2, 9, 7]);

echo("Original vector\n");

// Display the vector elements
print_r($vect);

// Use sort() function to sort
// the vector elements
$vect->sort(function($element1, $element2) {
    return $element2 <=> $element1;
});

echo("\nDecreasing Sorted elements\n");

// Display the sorted vector 
// elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.sort.php](http://php.net/manual/en/ds-vector.sort.php)
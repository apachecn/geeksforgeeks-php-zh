# PHP|Ds\Vector Sorted()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-sorted-function/](https://www.geeksforgeeks.org/php-dsvector-sorted-function/)

**ds\Vector：：sorted()**函数是 PHP 中的一个内置函数，用于通过创建原始向量的副本来对向量的元素进行排序。 这将使用默认比较器以升序排列向量元素。

**语法：**

```php
*Ds\Vector* public Ds\Vector::sorted( $comparator )

```

**参数：**此函数接受保存排序函数的单个参数*$compator*。

**返回值：**此函数返回已排序向量的副本。

下面的程序演示了 PHP 中的**ds\Vector：：sorted()**函数：

**程序 1：**

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector([6, 5, 4, 3, 2, 1]);

echo("Original vector\n");

// Display the vector elements
var_dump($vect);

// Use sorted() function to sort
// the copy of vector elements
$res = $vect->sorted();

echo("\nSorted elements\n");

// Display the sorted elements
var_dump($res);

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
var_dump($vect);

// Use sorted() function to sort
// the copy of vector elements
$res = $arr->sorted(function($element1, $element2) {
    return $element1 <=> $element2;
});

echo("\nSorted elements\n");

// Display the sorted elements
var_dump($res);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.sorted.php](http://php.net/manual/en/ds-vector.sorted.php)
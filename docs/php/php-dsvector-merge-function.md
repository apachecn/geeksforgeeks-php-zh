# PHP|Ds\Vector Merge()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-merge-function/](https://www.geeksforgeeks.org/php-dsvector-merge-function/)

**ds\Vector：：Merge()**函数是 PHP 中的一个内置函数，用于将所有元素合并到向量中。

**语法：**

```
*Ds\Vector* public Ds\Vector::merge( $values )
```

**参数：**此函数接受单个参数*$values*，该参数是可遍历的对象或数组。
**返回值：**此函数返回将元素合并到向量后向量的副本。

下面的程序说明了 PHP 中的**Ds\Vector：：Merge()**函数：

**程序 1：**

## PHP

```
<?php

// Create new vector
$arr1 = new \Ds\Vector([10, 20, 30, 40, 50]);

echo("Original vector elements\n");
print_r($arr1);

// Create new vector
$arr2 = new \Ds\Vector([60, 70, 80, 90, 100]);

echo("Vector Elements after merging\n");

// Use merge() function to merge two vector
// and display its resultant vector
print_r($arr1->merge($arr2));

?>
```

发帖主题：Re：Колибри0.7.0

```
Original vector elements
Ds\Vector Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
)
Vector Elements after merging
Ds\Vector Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => 40
    [4] => 50
    [5] => 60
    [6] => 70
    [7] => 80
    [8] => 90
    [9] => 100
)
```

**程序 2：**

## PHP

```
<?php

// Create new vector
$arr1 = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("Original vector elements\n");
print_r($arr1);

// Create new vector
$arr2 = new \Ds\Vector([60, 70, 100]);

echo("Vector Elements after merging\n");

// Use merge() function to merge two vector
// and display its resultant vector
print_r($arr1->merge($arr2));

?>
```

发帖主题：Re：Колибри0.7.0

```
Original vector elements
Ds\Vector Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
)
Vector Elements after merging
Ds\Vector Object
(
    [0] => geeks
    [1] => for
    [2] => geeks
    [3] => 60
    [4] => 70
    [5] => 100
)
```

**引用：**[http://php.net/manual/en/ds-vector.merge.php](http://php.net/manual/en/ds-vector.merge.php)
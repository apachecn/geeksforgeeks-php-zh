# PHP|ds\Vector filter()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-filter-function/](https://www.geeksforgeeks.org/php-dsvector-filter-function/)

**ds\Vector：：Filter()**函数用于过滤出仅满足回调函数中定义的条件的元素。 在对向量进行过滤后，它将剔除不满足函数中提到的条件的元素。

**语法：**

```
*Ds\Vector* public Ds\Vector::filter( $callback )
```

**参数：**此函数接受单个参数*$callback*，如果要包括向量中的元素，则返回 TRUE，否则返回 FALSE。

**返回值：**此函数返回包含根据可调用函数过滤的所有元素的向量。

以下程序说明了 PHP 中的**ds\Vector：：Filter()**函数：

**程序 1：**

```
<?php

// Create new vector element
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

echo "Original Vector elements\n";

// Display the vector element
var_dump($vector);

echo("\nElements greater than or equal to 4\n");

// Filter the vector element
var_dump($vector->filter(function($value) {
    return $value >= 4;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new vector element
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

echo "Original Vector elements\n";

// Display the vector element
var_dump($vector);

echo("\nOdd elements\n");

// Use filter() function to filter
// the vector element
var_dump($vector->filter(function($value) {
    return $value % 2 == 1;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.filter.php](http://php.net/manual/en/ds-vector.filter.php)
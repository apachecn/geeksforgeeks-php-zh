# PHP|ds\Vector unShift()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-unshift-function/](https://www.geeksforgeeks.org/php-dsvector-unshift-function/)

**ds\Vector：：unShift()**函数是 PHP 中的一个内置函数，用于将元素添加到向量的前面。 此函数将向量中的所有元素向前移动，并将新元素添加到前面。

**语法：**

```php
*void* public Ds\Vector::unshift( $values )

```

**参数：**此函数接受单个参数*$values*，该参数保存要添加到向量中的值。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Vector：：unShift()**函数：

**程序 1：**

```php
<?php

// Create new Vector
$vect = new \Ds\Vector([3, 6, 1, 2, 9, 7]);

echo("Original vector:\n");

// Display the vector elements
print_r($vect);

echo("\nArray elements after inserting new element\n");

// Use unshift() function to aff elements
$vect->unshift(10, 20, 30);

// Display updated vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new Vector
$vect = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("Original vector:\n");

// Display the vector elements
print_r($vect);

echo("\nArray elements after inserting new element\n");

// Use unshift() function to aff elements
$vect->unshift("PHP articles");

// Display updated vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.unshift.php](http://php.net/manual/en/ds-vector.unshift.php)
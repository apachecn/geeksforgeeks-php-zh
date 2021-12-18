# PHP|ds\Vector Rotate()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-rotate-function/](https://www.geeksforgeeks.org/php-dsvector-rotate-function/)

**Ds\Vector：：Rotate()**函数是 PHP 中的一个内置函数，用于按给定的旋转次数旋转数组元素。 旋转也会原地进行。

**语法：**

```
*void* public Ds\Vector::rotate( $rotations )

```

**参数：**此函数接受保存旋转次数的单个参数*$rotation*。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Vector：：Rotate()**函数：

**程序 1：**

```
<?php

// Create new Vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5]);

echo("Original Vector\n");

// Display the Vector elements
print_r($vect);

// Use rotate() function to rotate
// the vector elements
$vect->rotate(3);

echo("\nVector after rotating by 3 places\n");

// Display the Vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**当旋转数大于矢量中的元素数时。

```
<?php

// Create new Vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5]);

echo("Original Vector\n");

// Display the Vector elements
print_r($vect);

// Use rotate() function to rotate
// the vector elements
$vect->rotate(6);

echo("\nVector after rotating by 6 places\n");

// Display the Vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.rotate.php](http://php.net/manual/en/ds-vector.rotate.php)
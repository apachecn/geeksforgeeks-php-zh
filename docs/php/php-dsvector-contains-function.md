# PHP|ds\Vector 包含()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-contains-function/](https://www.geeksforgeeks.org/php-dsvector-contains-function/)

**ds\Vector：：CONTAINS()**函数是 PHP 中的一个内置函数，用于检查向量是否包含给定值。

**语法：**

```
*bool* public Ds\Vector::contains( $values )
```

**参数：**此函数接受包含单个/多个值的单个参数*$values*。

**返回值：**如果给定值存在，此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**ds\Vector：：CONTAINS()**函数：

**程序 1：**

```
<?php

// Create a vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Use contains() function to check
// existence of vector elements
var_dump($vector->contains(1));

var_dump($vector->contains(1, 2));

var_dump($vector->contains(10));

?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a vector
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

// Use contains() function to check
// existence of vector elements
var_dump($vector->contains("geeks"));

var_dump($vector->contains("geeks", "for"));

var_dump($vector->contains("GfG"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.contains.php](http://php.net/manual/en/ds-vector.contains.php)
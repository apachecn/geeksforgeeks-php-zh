# PHP|ds\Vector first()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-first-function/](https://www.geeksforgeeks.org/php-dsvector-first-function/)

**ds\Vector：：first()**函数是 PHP 中的一个内置函数，用于查找向量中的第一个元素。

**语法：**

```
*mixed* public Ds\Vector::first( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回向量中存在的第一个元素。

以下程序说明了 PHP 中的**ds\Vector：：First()**函数：

**程序 1：**

```
<?php

// Create vector elements
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

echo("First element of the vector: ");

// Use first() function to find
// the first element
var_dump($vector->first());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create vector elements
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("First element of the vector: ");

// Use first() function to find
// the first element
var_dump($vector->first());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.first.php](http://php.net/manual/en/ds-vector.first.php)
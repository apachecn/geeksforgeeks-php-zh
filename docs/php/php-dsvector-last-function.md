# PHP|ds\Vector last()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-last-function/](https://www.geeksforgeeks.org/php-dsvector-last-function/)

**ds\Vector：：last()**函数是 PHP 中的一个内置函数，用于返回向量的最后一个元素。

**语法：**

```php
*mixed* public Ds\Vector::last( void )

```

**参数：**此函数不包含任何参数。

**返回值：**此函数返回向量中最后一个索引处的值。

以下程序说明了 PHP 中的**ds\Vector：：last()**函数：

**程序 1：**

```php
<?php

// Create new vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

echo("Last element of vector: ");

// Use last() function to find the
// last element of vector
var_dump($vector->last());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new vector
$vector = new \Ds\Vector(["geeks", "for", "geeks", "practice"]);

// pop the vector element
$vector->pop();

echo("Last element of vector: ");

// Use last() function to find the
// last element of vector
var_dump($vector->last());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.last.php](http://php.net/manual/en/ds-vector.last.php)
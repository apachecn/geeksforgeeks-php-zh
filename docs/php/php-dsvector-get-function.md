# PHP|ds\Vector get()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-get-function/](https://www.geeksforgeeks.org/php-dsvector-get-function/)

**ds\Vector：：get()**函数是 PHP 中的一个内置函数，用于返回给定索引处的元素。

**语法：**

```
*mixed* public Ds\Vector::get( $index )

```

**参数：**此函数接受单个参数*$index*，该参数包含要返回元素的索引(从 0 开始的索引)。

**返回值：**此函数返回向量中给定索引处的元素。

**异常**：如果索引无效，则此函数返回*OutOfRangeException*。

以下程序说明了 PHP 中的**Ds\Vector：：Get()**函数：

**程序 1：**

```
<?php

// Create new Vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Use get() function to find the 
// element at given index
var_dump($vector->get(3));

var_dump($vector->get(1));

var_dump($vector->get(4));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new Vector
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

// Use get() function to find the 
// element at given index
var_dump($vector->get(0));

var_dump($vector->get(1));

var_dump($vector->get(2));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.get.php](http://php.net/manual/en/ds-vector.get.php)
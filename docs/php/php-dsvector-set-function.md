# PHP|ds\Vector set()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-set-function/](https://www.geeksforgeeks.org/php-dsvector-set-function/)

**ds\Vector：：Set()**函数是 PHP 中的一个内置函数，用于在给定索引处设置向量中的值。

**语法：**

```
*void* public Ds\Vector::set( $index, $value )

```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$index:** this parameter holds the index value of the vector value to update.
*   **$VALUE:** this parameter holds the value of the previous element to be replaced.

**返回值：**此函数不返回任何值。

**异常：**如果索引无效，此函数将引发*OutOfRangeException*。

以下程序说明了 PHP 中的**ds\Vector：：Set()**函数：

**程序 1：**

```
<?php

// Create new Vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5]);

// Display the Vector elements
print_r($vect);

// Use set() function to set the 
// element in the vector
$vect->set(1, 10);

echo("\nVector after updating the element\n");

// Display the vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new Vector
$vect = new \Ds\Vector(["geeks", "of", "geeks"]);

// Display the Vector elements
print_r($vect);

// Use set() function to set the 
// element in the vector
$vect->set(1, "for");

echo("\nVector after updating the element\n");

// Display the vector elements
print_r($vect);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.set.php](http://php.net/manual/en/ds-vector.set.php)
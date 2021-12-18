# PHP|ds\Vector map()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-map-function/](https://www.geeksforgeeks.org/php-dsvector-map-function/)

**ds\Vector：：map()**函数是 PHP 中的一个内置函数，用于在应用于向量中的每个值后返回回调结果。

**语法：**

```
*Ds\Vector* public Ds\Vector::map( $callback )

```

**参数：**此函数接受要应用于每个向量元素的单个参数*$callback*。

**返回值：**对向量中的每个值应用回调后，此函数返回向量。

下面的程序说明了 PHP 中的**ds\Vector：：map()**函数：

**程序 1：**

```
<?php

// Create new Vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Display the Vector element after
// applying the callback function
print_r($vector->map(function($value) { 
    return $value * 10; 
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**此程序显示*MAP*()函数的实现，该函数为满足回调条件的每个元素在向量中设置 1。

```
<?php

// Create new Vector
$vector = new \Ds\Vector([10, 20, 30, 40, 50]);

// Display the Vector element after
// applying the callback function
print_r($vector->map(function($value) { 
    return $value <= 30;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.map.php](http://php.net/manual/en/ds-vector.map.php)
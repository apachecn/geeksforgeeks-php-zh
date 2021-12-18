# PHP|ds\Vector Capacity()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-capacity-function/](https://www.geeksforgeeks.org/php-dsvector-capacity-function/)

**ds\Vector：：Capacity()**函数是 PHP 中的内置函数，用于返回向量的当前容量。

**语法：**

```
*int* public Ds\Vector::capacity( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前向量的容量。

以下程序说明了 PHP 中的**ds\Vector：：Capacity()**函数：

**程序 1：**

```
<?php

// Declare a vector
$vector = new \Ds\Vector();

// Use capacity() function to 
// find the vector capacity 
// and display it
var_dump($vector->capacity());

// Use push() function to add 
// vector element
$vector->push(...range(1, 20));

// Display the vector capacity
var_dump($vector->capacity());

?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Declare a vector
$vector = new \Ds\Vector();

// Use capacity() function to 
// find the vector capacity 
// and display it
var_dump($vector->capacity());

// Use push() function to add 
// vector element
$vector->push(...range(1, 100));

// Display the vector capacity
var_dump($vector->capacity());

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.capacity.php](http://php.net/manual/en/ds-vector.capacity.php)
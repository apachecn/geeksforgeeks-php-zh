# PHP|ds\Vector Shift()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-shift-function/](https://www.geeksforgeeks.org/php-dsvector-shift-function/)

**ds\Vector：：Shift()**函数是 PHP 中的一个内置函数，用于从向量中删除第一个元素并返回它。

**语法：**

```php
*mixed* public Ds\Vector::shift( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回索引 0 处的值。

**异常：**如果 Vector 为空，则此函数引发*UnderflowException*。

以下程序说明了 PHP 中的**ds\Vector：：Shift()**函数：

**程序 1：**

```php
<?php

// Declare an Vector
$vect = new \Ds\Vector(["geeks", "of", "geeks"]);

echo("First element in the vector:\n");

// Use shift() function to remove first 
// element from vector and display it
var_dump($vect->shift());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare an Vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5, 6]);

// Use shift() function to remove first 
// element from vector and display it
var_dump($vect->shift());

var_dump($vect->shift());

var_dump($vect->shift());

var_dump($vect->shift());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.shift.php](http://php.net/manual/en/ds-vector.shift.php)
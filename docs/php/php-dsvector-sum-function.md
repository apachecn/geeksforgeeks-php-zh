# PHP|ds\Vector sum()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-sum-function/](https://www.geeksforgeeks.org/php-dsvector-sum-function/)

**ds\Vector：：sum()**函数是 PHP 中的一个内置函数，它返回向量的所有元素的总和。

**语法：**

```php
*number* public Ds\Vector::sum( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回向量中所有元素的总和。 总和可以是整型或浮点型，具体取决于矢量元素。

以下程序说明了 PHP 中的**ds\Vector：：sum()**函数：

**程序 1：**

```php
<?php

// Declare the new Vector
$arr = new \Ds\Vector([3, 6, 1, 2, 9, 7]);

echo("Original vector:\n");

// Display the vector elements
var_dump($arr);

echo("\nSum of elements:\n");

// Use sum() function to returns the 
// sum of all vector elements
var_dump($arr->sum());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare the new Vector
$arr = new \Ds\Vector([3.5, 6, 1, 2.7, 9, 7.3]);

echo("Original vector:\n");

// Display the vector elements
print_r($arr);

echo("\nSum of elements: ");

// Use sum() function to returns the 
// sum of all vector elements
print_r($arr->sum());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.sum.php](http://php.net/manual/en/ds-vector.sum.php)
# PHP|ds\Vector count()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-count-function/](https://www.geeksforgeeks.org/php-dsvector-count-function/)

**ds\Vector：：count()**函数是 PHP 中的一个内置函数，用于计算向量中的元素数。

**语法：**

```
*int* public Ds\Vector::count( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回向量中的元素数。

下面的程序说明了 PHP 中的**ds\Vector：：count()**函数：

**程序 1：**

```
<?php

// Declare a vector 
$arr1 = new \Ds\Vector([1, 2, 3, 4, 5, 6, 7, 8]);

echo("Vector elements\n");

// Display the vector elements
print_r($arr1);

echo("Count vector elements: ");

// Use count() function to count 
// elements in the vector
echo(count($arr1));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Declare a vector 
$arr1 = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("Vector elements\n");

// Display the vector elements
print_r($arr1);

echo("Count vector elements: ");

// Use count() function to count 
// elements in the vector
echo(count($arr1));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.count.php](http://php.net/manual/en/ds-vector.count.php)
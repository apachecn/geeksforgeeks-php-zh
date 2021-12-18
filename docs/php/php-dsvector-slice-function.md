# PHP|ds\Vector Slice()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-slice-function/](https://www.geeksforgeeks.org/php-dsvector-slice-function/)

**ds\Vector：：Slice()**函数是 PHP 中的一个内置函数，用于返回给定向量的子向量。

**语法：**

```php
*Ds\Vector* public Ds\Vector::slice( $index, $length )/pre>

Parameters: This function accepts two parameter as mentioned above and described below:

```

*   **$index：**此参数保存子向量的起始索引。 指标值可以是正的，也可以是负的。 如果索引值为正，则从向量的索引开始，如果索引值为负，则从结束处开始。
*   **$Length：**此参数保存子向量的长度。 此参数可以采用正值和负值。 如果长度为正，则子向量大小等于给定长度，如果长度为负，则向量将从末尾停止那么多值。

**Return Value:** This function returns a sub-vector of given range. Below programs illustrate the **Ds\Vector::slice()** function in PHP: **Program 1:**

```php
<?php 

// Create new vector 
$vect = new \Ds\Vector([1, 2, 3, 4, 5, 6]); 

echo("Original vector:\n"); 

// Display the vector element 
var_dump($vect); 

// Use slice() function to  
// create sub vector 
$res = $vect->slice(1, 2); 

echo("\nNew sub-vector\n"); 

// Display the sub-vector elements 
var_dump($res); 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
Original vector:
object(Ds\Vector)#1 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}

New sub-vector
object(Ds\Vector)#2 (2) {
  [0]=>
  int(2)
  [1]=>
  int(3)
}

```

**程序 2：**

```php
<?php

// Create new vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5, 6]);

echo("Original vector:\n");

// Display the vector element
var_dump($vect);

// Use slice() function to 
// create sub vector
$res = $vect->slice(2, -2);

echo("\nNew sub-vector\n");

// Display the sub-vector elements
var_dump($res);

$res = $vect->slice(4);

echo("\nNew sub-vector\n");

// Display the sub-vector elements
var_dump($res);

?>
```

发帖主题：Re：Колибри0.7.0

```php
Original vector:
object(Ds\Vector)#1 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}

New sub-vector
object(Ds\Vector)#2 (2) {
  [0]=>
  int(3)
  [1]=>
  int(4)
}

New sub-vector
object(Ds\Vector)#3 (2) {
  [0]=>
  int(5)
  [1]=>
  int(6)
}

```

**引用：**[http://php.net/manual/en/ds-vector.slice.php](http://php.net/manual/en/ds-vector.slice.php)
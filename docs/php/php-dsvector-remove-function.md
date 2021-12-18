# PHP|ds\Vector Remove()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-remove-function/](https://www.geeksforgeeks.org/php-dsvector-remove-function/)

**ds\Vector：：Remove()**函数是 PHP 中的一个内置函数，用于就地反转向量的元素。 例如，如果向量元素是[1，2，3，4，5]，那么它将被反转为[5，4，3，2，1]。

**语法：**

```php
*mixed* public Ds\Vector::remove( $index )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Vector：：Remove()**函数：

**程序 1：**

## PHP

```php
<?php

// Declare new Vector
$arr = new \Ds\Vector([1, 2, 3, 4, 5, 6]);

echo("Vector Elements\n");

// Display the Vector elements
var_dump($arr);

// Use reverse() function to 
// reverse Vector elements
$arr->reverse();

echo("\nVector after reversing\n");

// Display the vector elements
var_dump($arr);

?>
```

**Output:**

```php
Vector Elements
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

Vector after reversing
object(Ds\Vector)#1 (6) {
  [0]=>
  int(6)
  [1]=>
  int(5)
  [2]=>
  int(4)
  [3]=>
  int(3)
  [4]=>
  int(2)
  [5]=>
  int(1)
}

```

**程序 2：**

## PHP

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector(["Learn", "data", "structures"]);

echo("Vector Elements\n");

// Display the Vector elements
print_r($vect);

// Use reverse() function to 
// reverse Vector elements
$vect->reverse();

echo("\nVector after reversing\n");

// Display the vector elements
print_r($vect);

?>
```

**Output:**

```php
Vector Elements
Ds\Vector Object
(
    [0] => Learn
    [1] => data
    [2] => structures
)

Vector after reversing
Ds\Vector Object
(
    [0] => structures
    [1] => data
    [2] => Learn
)

```

**引用：**[http://php.net/manual/en/ds-vector.reverse.php](http://php.net/manual/en/ds-vector.reverse.php)
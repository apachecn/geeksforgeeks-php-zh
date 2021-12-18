# PHP|ds\Vector toArray()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-toarray-function/](https://www.geeksforgeeks.org/php-dsvector-toarray-function/)

**ds\Vector：：toArray()**函数是 PHP 中的内置函数，用于将向量转换为数组。 向量的所有元素都被复制到数组中。
**语法：**和

```php
*array* public Ds\Vector::toArray( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回包含向量的所有元素的数组。
以下程序说明 PHP：
**程序 1：**和
中的**Ds\Vector：：toArray()**函数

## PHP

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector([3, 6, 1, 2, 9, 7]);

echo("Original vector\n");

// Display the vector elements
var_dump($vect);

echo("\nArray elements\n");

// Use toArray() function to convert
// vector to array and display it
var_dump($vect->toArray());

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
Original vector
object(Ds\Vector)#1 (6) {
  [0]=>
  int(3)
  [1]=>
  int(6)
  [2]=>
  int(1)
  [3]=>
  int(2)
  [4]=>
  int(9)
  [5]=>
  int(7)
}

Array elements
array(6) {
  [0]=>
  int(3)
  [1]=>
  int(6)
  [2]=>
  int(1)
  [3]=>
  int(2)
  [4]=>
  int(9)
  [5]=>
  int(7)
}
```

**程序 2：**

## PHP

```php
<?php

// Declare new Vector
$vect = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("Original vector\n");

// Display the vector elements
var_dump($vect);

echo("\nArray elements\n");

// Use toArray() function to convert
// vector to array and display it
var_dump($vect->toArray());

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
Original vector
object(Ds\Vector)#1 (3) {
  [0]=>
  string(5) "geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "geeks"
}

Array elements
array(3) {
  [0]=>
  string(5) "geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "geeks"
}
```

**引用：**[http://php.net/manual/en/ds-vector.toarray.php](http://php.net/manual/en/ds-vector.toarray.php)
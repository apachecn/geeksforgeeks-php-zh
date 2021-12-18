# PHP|ds\Vector POP()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-pop-function/](https://www.geeksforgeeks.org/php-dsvector-pop-function/)

**ds\Vector：：op()**函数是 PHP 中的一个内置函数，用于删除向量的最后一个元素并返回它。

**语法：**

```php
*mixed* public Ds\Vector::pop( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回从向量中移除的最后一个元素。

下面的程序说明了 PHP 中的**ds\Vector：：op()**函数：

**程序 1：**

```php
<?php

// Create new Vector
$arr1 = new \Ds\Vector([10, 20, 30, 40, 50]);

echo("Original vector elements\n");
print_r($arr1);

echo("Last element in vector: ");

// Use pop() function to remove
// last element from vector
var_dump($arr1->pop());

echo("\nVector after removing the last element\n");
print_r($arr1);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new Vector
$arr1 = new \Ds\Vector(["geeks", "for", "geeks"]);

echo("Original vector elements\n");
print_r($arr1);

echo("Last element in vector: ");

// Use pop() function to remove
// last element from vector
var_dump($arr1->pop());

echo("\nVector after removing the last element\n");
print_r($arr1);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.pop.php](http://php.net/manual/en/ds-vector.pop.php)
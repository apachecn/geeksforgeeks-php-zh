# PHP|ds\Vector Remove()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-remove-function-2/](https://www.geeksforgeeks.org/php-dsvector-remove-function-2/)

Ds\Vector：：Remove()函数是 PHP 中的一个内置函数，用于从索引中删除值并返回它。

**语法：**

```
*public* Ds\Vector::remove( $index ) : mixed

```

**参数：**此函数接受单个参数*$index*，该参数保存要删除元素的索引。

**返回值：**此函数返回删除的值。

**异常：**如果给定索引超出范围或无效，此函数将引发*OutOfRangeException*。

下面的程序说明了 PHP 中的 Ds\Vector：：Remove()函数：

**程序 1：**

```
<?php

// Declare new vector
$vect = new \Ds\Vector(["geeks", "for",
            "geeks", "DataStructures"]);

echo("Vector Elements\n");

// Display the Vector elements
print_r($vect);

echo("\nLast element of the vector: \n");

// Use remove() function to remove 
// value at index 3 and return it
var_dump($vect->remove(3));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Declare new vector
$vect = new \Ds\Vector([1, 2, 3, 4, 5, 6]);

echo("Vector Elements\n");

// Display the Vector elements
print_r($vect);

echo("\nLast element of the vector: \n");

// Use remove() function to remove 
// value at index 3 and return it
var_dump($vect->remove(3));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.remove.php](http://php.net/manual/en/ds-vector.remove.php)
# PHP|Ds\Vector Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-reversed-function/](https://www.geeksforgeeks.org/php-dsvector-reversed-function/)

Ds\Vector：：Reverse()函数是 PHP 中的一个内置函数，用于在将原始向量的元素复制到副本中后反转向量的元素。

**语法：**

```
*public* Ds\Vector::reversed( void ) : Ds\Vector

```

**参数：**此函数不接受任何参数。

**返回值：**此函数以相反的顺序返回原始向量的副本。 此外，原始向量也不会有任何效果。

下面的程序演示了 PHP 中的 Ds\Vector：：Reverse()函数：

**程序 1：**

```
<?php

// Create new Vector
$arr = new \Ds\Vector([1, 2, 3, 4, 5]);

// Display the elements
var_dump($arr);

echo("Vector after reversing\n");

// Use reversed() function to reverse 
// the copy of vector and display it
var_dump($arr->reversed());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new Vector
$arr = new \Ds\Vector(["Learn", "data", "structures"]);

// Display the elements
print_r($arr);

echo("Vector after reversing\n");

// Use reversed() function to reverse 
// the copy of vector and display it
print_r($arr->reversed());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.reversed.php](http://php.net/manual/en/ds-vector.reversed.php)
# PHP|ds\Vector copy()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-copy-function/](https://www.geeksforgeeks.org/php-dsvector-copy-function/)

**ds\Vector：：copy()**函数是 PHP 中的一个内置函数，用于创建给定向量的副本。

**语法：**

```
*Ds\Vector* public Ds\Vector::copy( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回向量的浅表副本。

以下程序说明了 PHP 中的**ds\Vector：：copy()**函数：

**程序 1：**

```
<?php

// Create a vector array
$arr1 = new \Ds\Vector([1, 2, 3, 5]);

// Use copy() function to copy
// the vector array
$arr2 = $arr1->copy();

echo("Original Array \n");

// Display the original array
print_r($arr1);

echo("Copied Array \n");

// Display the copied array
print_r($arr2);

?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a vector array
$arr1 = new \Ds\Vector(["geeks", "for", "geeks"]);

// Use copy() function to copy
// the vector array
$arr2 = $arr1->copy();

echo("Original Array\n");

// Display the original array
print_r($arr1);

echo("Copied Array\n");

// Display the copied array
print_r($arr2);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.copy.php](http://php.net/manual/en/ds-vector.copy.php)
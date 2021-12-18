# PHP|Ds\Vector find()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-find-function/](https://www.geeksforgeeks.org/php-dsvector-find-function/)

**ds\Vector：：find()**函数是 PHP 中的一个内置函数，用于查找向量中元素的索引。

**语法：**

```php
*mixed* public Ds\Vector::find( $value )

```

**参数：**此函数接受需要查找索引值的单个参数*$value*。

**返回值：**此函数成功时返回向量中元素的索引，失败时返回 False。

以下程序说明了 PHP 中的**ds\Vector：：find()**函数：

**程序 1：**

```php
<?php

// Declare a Vector elements
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Display the vector elements
var_dump($vector);

// Use find() function to find 
// the index value of element
var_dump($vector->find(1));

var_dump($vector->find(5));

var_dump($vector->find(8));

var_dump($vector->find("Geeks"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare a Vector elements
$vector = new \Ds\Vector(["Geeks", "for",
                "Geek", 1, "1", 0, "0"]);

// Use find() function to find 
// the index value of element
var_dump($vector->find(1));

var_dump($vector->find("0"));

var_dump($vector->find(8));

var_dump($vector->find("Geeks"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.find.php](http://php.net/manual/en/ds-vector.find.php)
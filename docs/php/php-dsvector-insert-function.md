# PHP|Ds\Vector Insert()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-insert-function/](https://www.geeksforgeeks.org/php-dsvector-insert-function/)

**Ds\Vector：：Insert()**函数是 PHP 中的一个内置函数，用于将元素插入到给定索引处的向量中。

**语法：**

```php
*void* public Ds\Vector::insert( $index, $values )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$index:** this parameter holds the index of the element to be inserted.
*   **$value:** this parameter holds the value to be inserted.

**返回值：**此函数不返回任何值。

**异常**：如果索引无效，则此函数返回*OutOfRangeException*。

下面的程序演示了 PHP 中的**ds\Vector：：Insert()**函数：

**程序 1：**

```php
<?php

// Declare new vector
$vector = new \Ds\Vector([1, 2, 4, 5]);

// Display the Vector element
print_r($vector);

// Use insert() function to add 
// element in the vector
$vector->insert(2, 3);

// Display the vector element
print_r($vector);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare new vector
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

// Display the Vector element
print_r($vector);

// Use insert() function to add 
// element in the vector
$vector->insert(1, "practice");

// Display the vector element
print_r($vector);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.insert.php](http://php.net/manual/en/ds-vector.insert.php)
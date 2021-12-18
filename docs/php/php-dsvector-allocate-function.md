# PHP|Ds\矢量分配()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-allocate-function/](https://www.geeksforgeeks.org/php-dsvector-allocate-function/)

**ds\Vector：：Allocation()**函数是 PHP 中的一个内置函数，用于为所需的容量分配足够的内存。 它提供用于分配空间的向量的自定义大小。

**语法：**

```php
*void* public Ds\Vector::allocate( $capacity ) 

```

**参数：**此函数接受单个参数**$acity**，该参数保存要分配的空间。

**注意：如果此值小于或等于当前容量，**容量将保持不变。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**Ds\Vector：：Allocation()**函数：

**程序 1：**

```php
<?php

// Declare new vector
$vector = new \Ds\Vector();

echo("Allocated Space is: ");

// Use capacity() function
var_dump($vector->capacity());

echo("Allocated space is: ");

// Use allocate() function to 
// allocate capacity
$vector->allocate(50);

// Display the allocated vector
// capacity
var_dump($vector->capacity());

?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare new vector
$vector = new \Ds\Vector();

echo("Allocated Space is: ");

// Use capacity() function
var_dump($vector->capacity());

echo("Allocated space is: ");

// Use allocate() function to 
// allocate capacity
$vector->allocate(5);

// Display the Vector capacity
var_dump($vector->capacity());

// Use allocate() function to 
// allocate capacity
$vector->allocate(120);

// Display the Vector capacity
var_dump($vector->capacity());
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.allocate.php](http://php.net/manual/en/ds-vector.allocate.php)
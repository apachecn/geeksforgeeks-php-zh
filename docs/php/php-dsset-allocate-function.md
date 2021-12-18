# PHP|ds\Set ALLOCATE()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-allocate-function/](https://www.geeksforgeeks.org/php-dsset-allocate-function/)

**ds\set：：Allocation()**函数是 PHP 中的一个内置函数，用于为所需的容量分配内存。

**语法：**

```
*void* public Ds\Set::allocate( $capacity )
```

**参数：**此函数接受单个参数*$Capacity*，该参数保存要分配的容量的值。 容量总是以 2 的幂四舍五入。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**Ds\Set：：Allocation()**函数：

**程序 1：**

```
<?php 

// Declare new empty set 
$set = new \Ds\Set(); 

echo("Allocated Space is: "); 

// Use capacity() function 
var_dump($set->capacity());  

// Use allocate() function to 
// allocate capacity 
$set->allocate(50); 

echo("Allocated space is: ");

// Display the allocated vector 
// capacity 
var_dump($set->capacity()); 

?> 
```

**输出：**

```
Allocated Space is: int(8)
Allocated space is: int(64)

```

**程序 2：**

```
<?php 

// Declare an empty set 
$set = new \Ds\Set();

echo("Allocated Space is: "); 

// Use capacity() function 
var_dump($set->capacity());  

// Use allocate() function to 
// allocate capacity 
$set->allocate(5); 

echo("Allocated space is: ");

// Display the capacity 
var_dump($set->capacity()); 

echo("Allocated space is: ");

// Use allocate() function to 
// allocate capacity 
$set->allocate(120); 

// Display the capacity 
var_dump($set->capacity()); 
?> 
```

**输出：**

```
Allocated Space is: int(8)
Allocated space is: int(8)
Allocated space is: int(128)

```

**引用：**[http://php.net/manual/en/ds-set.allocate.php](http://php.net/manual/en/ds-set.allocate.php)
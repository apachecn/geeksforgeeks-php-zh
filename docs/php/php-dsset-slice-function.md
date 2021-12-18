# PHP|ds\Set Slice()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-slice-function/](https://www.geeksforgeeks.org/php-dsset-slice-function/)

**ds\set：：Slice()**函数是 PHP 中的内置函数，用于返回给定范围的子集。

**语法：**

```php
*Ds\Set* public Ds\Set::slice ( int $index [, int $length ] )

```

参数：此函数接受上述两个参数：

*   **$index:** this parameter holds the starting index of the subset. The indicator value can be positive or negative. If the index value is positive, it starts at the index of the collection, and if the index value is negative, the collection starts at the end.
*   **$Length:** this parameter saves the length of the subset. This parameter can take positive and negative values. If the length is positive, the subset size is equal to the given length, and if the length is negative, the collection stops so many values from the end.

**返回值：**此函数返回给定范围的子集。

下面的程序演示了 PHP 中的**ds\set：：Slice()**函数：

**程序 1：**

```php
<?php 

// Create new set 
$set = new \Ds\Set([1, 3, 6, 9, 10, 15, 20]); 

// Use slice() function to create 
// sub-set and display it 
print_r($set->slice(2)); 

print_r($set->slice(1, 2)); 

print_r($set->slice(2, -2)); 

?> 
```

**输出：**

```php
Ds\Set Object
(
    [0] => 6
    [1] => 9
    [2] => 10
    [3] => 15
    [4] => 20
)
Ds\Set Object
(
    [0] => 3
    [1] => 6
)
Ds\Set Object
(
    [0] => 6
    [1] => 9
    [2] => 10
)

```

**程序 2：**

```php
<?php 

// Create new set
$set = new \Ds\Set(["Geeks", "GFG", "Abc", "for"]); 

// Use slice() function to create 
// sub-set and display it 
print_r($set->slice(3)); 

print_r($set->slice(2, 0)); 

print_r($set->slice(0, 3)); 

?> 
```

**输出：**

```php
Ds\Set Object
(
    [0] => for
)
Ds\Set Object
(
)
Ds\Set Object
(
    [0] => Geeks
    [1] => GFG
    [2] => Abc
)

```

**引用：**[https://www.php.net/manual/en/ds-set.slice.php](https://www.php.net/manual/en/ds-set.slice.php)
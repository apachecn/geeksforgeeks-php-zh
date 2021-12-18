# PHP|ds\set copy()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-copy-function/](https://www.geeksforgeeks.org/php-dsset-copy-function/)

**ds\set：：copy()**函数是 PHP 中的内置函数，用于返回 set 元素的副本。

**语法：**

```
*Ds\Set* public Ds\Set::copy( void )
```

**参数：**此函数不包含任何参数。

**返回值：**返回集合元素的副本。

以下程序说明了 PHP 中的**ds\set：：copy()**函数：

**程序 1：**

```
<?php 

// Create new Set 
$set = new \Ds\Set([10, 15, 21, 13, 16, 18]); 

// Display the Set element 
print_r($set); 

// Use copy() function
$set->copy(); 

// Display the Set element 
print_r($set); 

?> 
```

**输出：**

```
Ds\Set Object
(
    [0] => 10
    [1] => 15
    [2] => 21
    [3] => 13
    [4] => 16
    [5] => 18
)
Ds\Set Object
(
    [0] => 10
    [1] => 15
    [2] => 21
    [3] => 13
    [4] => 16
    [5] => 18
)

```

**程序 2：**

```
<?php 

// Create new Set 
$set = new \Ds\Set(["Geeks", "GFG", "ABC"]); 

// Display the Set element 
print_r($set); 

// Use copy() function
$set->copy(); 

// Display the Set element 
print_r($set); 

?> 
```

**输出：**

```
Ds\Set Object
(
    [0] => Geeks
    [1] => GFG
    [2] => ABC
)
Ds\Set Object
(
    [0] => Geeks
    [1] => GFG
    [2] => ABC
)

```

**引用：**[http://php.net/manual/en/ds-set.copy.php](http://php.net/manual/en/ds-set.copy.php)
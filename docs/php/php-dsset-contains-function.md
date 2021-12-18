# PHP|DS\SET CONTAINS()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-contains-function/](https://www.geeksforgeeks.org/php-dsset-contains-function/)

**Ds\Set：：CONTAINS()**函数是 PHP 中的内置函数，用于检查给定值是否存在于集合中。 此函数用于比较该值及其类型。

**语法：**

```
*bool* public Ds\Set::contains( $values )
```

**参数：**此函数接受单个或多个值，这些值需要检查集合中是否存在值。

**返回值：**如果集合中存在值，则返回 True，否则返回 False。

以下程序说明了 PHP 中的**Ds\Set：：CONTAINS()**函数：

**程序 1：**

```
<?php 

// Declare new Set
$set = new \Ds\Set(['G', 'e', 'e', 'k', 's', 5, 2, 7]); 

// Use contains() function to check elements 
// exist in the Set or not 
var_dump($set->contains('G'));  

var_dump($set->contains('k')); 

var_dump($set->contains('p'));  

var_dump($set->contains(7));  

var_dump($set->contains('5'));  

?>  
```

**输出：**

```
bool(true)
bool(true)
bool(false)
bool(true)
bool(false)

```

**程序 2：**

```
<?php 

// Declare new Set
$set = new \Ds\Set(['G', 'e', 'e', 'k', 's', 5, 2, 7]); 

// Use contains() function to check elements 
// exist in the Set or not 
var_dump($set->contains('G', 'e'));  

var_dump($set->contains('k', 'e', 7)); 

var_dump($set->contains('p', '1'));  

var_dump($set->contains(7, 1));  

var_dump($set->contains('5', 5));  

?>  
```

**输出：**

```
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)

```

**引用：**[http://php.net/manual/en/ds-set.contains.php](http://php.net/manual/en/ds-set.contains.php)
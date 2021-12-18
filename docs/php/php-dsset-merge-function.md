# PHP|ds\Set Merge()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-merge-function/](https://www.geeksforgeeks.org/php-dsset-merge-function/)

**ds\set：：merge()**函数是 PHP 中的一个内置函数，它在将所有给定值添加到集合后返回集合。

**语法：**

```php
*Ds\Set* public Ds\Set::merge ( mixed $values ) 

```

**参数：**此函数接受包含元素的单个参数**$values**。

**返回值：**此函数返回将所有元素相加的集合。

下面的程序说明了 PHP 中的**ds\set：：merge()**函数：

**程序 1：**

```php
<?php 

// Create new set
$set = new \Ds\Set([12, 15, 18, 20]); 

// Merge the set element and display it 
var_dump($set->merge([1, 2, 3])); 

// Display the set element 
var_dump($set) 
?> 
```

**输出：**

```php
object(Ds\Set)#2 (7) {
  [0]=>
  int(12)
  [1]=>
  int(15)
  [2]=>
  int(18)
  [3]=>
  int(20)
  [4]=>
  int(1)
  [5]=>
  int(2)
  [6]=>
  int(3)
}
object(Ds\Set)#1 (4) {
  [0]=>
  int(12)
  [1]=>
  int(15)
  [2]=>
  int(18)
  [3]=>
  int(20)
}

```

**程序 2：**

```php
<?php 

// Create new set
$set = new \Ds\Set([12, 15, 18, 20]); 

// Merge the set element and display it 
var_dump($set->merge(["G", "E", "E", "k", "S"])); 

?> 
```

**输出：**

```php
object(Ds\Set)#2 (8) {
  [0]=>
  int(12)
  [1]=>
  int(15)
  [2]=>
  int(18)
  [3]=>
  int(20)
  [4]=>
  string(1) "G"
  [5]=>
  string(1) "E"
  [6]=>
  string(1) "k"
  [7]=>
  string(1) "S"
}

```

**引用：**[https://www.php.net/manual/en/ds-set.merge.php](https://www.php.net/manual/en/ds-set.merge.php)
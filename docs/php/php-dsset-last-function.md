# PHP|ds\set last()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-last-function/](https://www.geeksforgeeks.org/php-dsset-last-function/)

**ds\set：：last()**函数是 PHP 中的内置函数，用于返回 Set 实例中的最后一个元素。

**语法：**

```
*void* public Ds\Set::last( void ) 
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回集合的最后一个值。

以下程序说明了 PHP 中的**ds\set：：last()**函数：

**程序 1：**

## PHP

```
<?php

// PHP program to illustrate the
// Ds\set::last() function

// Create a set instance
$set = new \Ds\Set();

// Adding elements to Set
$set->add("Welcome");
$set->add("to");
$set->add("GfG");

// Print the last element from set
print_r($set->last());

?>
```

**Output:** 

```
GfG
```

**程序 2：**

## PHP

```
<?php

// PHP program to illustrate the
// Ds\set::last() function

// Create a set instance
$set = new \Ds\Set();

// Adding elements to Set
$set->add("10");
$set->add("20");
$set->add("30");

// Print the last element from set
print_r($set->last());

?>
```

**Output:** 

```
30
```

**引用：**[http://php.net/manual/en/ds-set.last.php](http://php.net/manual/en/ds-set.first.php)
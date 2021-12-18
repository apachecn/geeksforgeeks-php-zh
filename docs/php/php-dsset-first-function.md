# PHP|ds\set first()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-first-function/](https://www.geeksforgeeks.org/php-dsset-first-function/)

**ds\set：：first()**函数是 PHP 中的内置函数，它返回集合的第一个元素。

**语法：**

```
*void* public Ds\Set::first( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回集合的第一个值。

下面的程序说明了 PHP 中的**ds\set：：first()**函数：

**程序 1**：

## PHP

```
<?php

// PHP program to illustrate the
// Ds\set::first() function

// Create a set instance
$set = new \Ds\Set();

// Adding elements to Set
$set->add("Welcome");
$set->add("to");
$set->add("GfG");

// Print the first element from set
print_r($set->first());

?>
```

**Output:** 

```
Welcome
```

**程序 2**：

## PHP

```
<?php

// PHP program to illustrate the
// Ds\set::first() function

// Create a set instance
$set = new \Ds\Set();

// Adding elements to Set
$set->add("10");
$set->add("20");
$set->add("30");

// Print the first element from set
print_r($set->first());

?>
```

**Output:** 

```
10
```

**引用：**[http://php.net/manual/en/ds-set.first.php](http://php.net/manual/en/ds-set.first.php)
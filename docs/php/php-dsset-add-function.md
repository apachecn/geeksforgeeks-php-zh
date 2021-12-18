# PHP|ds\set add()函数

> Original: [https://www.geeksforgeeks.org/php-dsset-add-function/](https://www.geeksforgeeks.org/php-dsset-add-function/)

**ds\set：：add()**函数是 PHP 中的一个内置函数，用于将值添加到集合中。

**语法：**

```php
*void* public Ds\Set::add( $values )
```

**参数：**此函数接受单个参数*$values*，该参数包含多个要添加到集合中的值。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\set：：add()**函数：

**程序 1：**

```php
<?php

// Declare an empty set
$set = new \Ds\Set();

// Use add() function to
// add elements to the set
$set->add(1);

$set->add("Geeks");

$set->add("G");

$set->add(10);

var_dump($set);
?>
```

**输出：**

```php
object(Ds\Set)#1 (4) {
  [0]=>
  int(1)
  [1]=>
  string(5) "Geeks"
  [2]=>
  string(1) "G"
  [3]=>
  int(10)
}

```

**程序 2：**

```php
<?php

// Declare an empty set
$set = new \Ds\Set();

// Use add() function to
// add elements to the set
$set->add(10, 20, 30, "Geeks", "for");

print_r($set);
?>
```

**输出：**

```php
Ds\Set Object
(
    [0] => 10
    [1] => 20
    [2] => 30
    [3] => Geeks
    [4] => for
)

```

**引用：**[http://php.net/manual/en/ds-set.add.php](http://php.net/manual/en/ds-set.add.php)
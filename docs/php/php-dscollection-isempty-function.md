# PHP|ds\Collection isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-dscollection-isempty-function/](https://www.geeksforgeeks.org/php-dscollection-isempty-function/)

Ds\Collection：：isEmpty()函数是 PHP 中的一个内置函数，用于返回集合是否为空。

**语法：**

```
Ds\Collection::isEmpty ( void ) : bool
```

**参数：**此函数不接受任何参数。

**返回值：**如果集合为空，则返回 True，否则返回 False。

下面的程序说明了 PHP 中的 ds\Collection：：isEmpty()函数：

**示例 1：**

```
<?php

// Create a collection
$collection = new \Ds\Vector([10, 15, 21, 13, 16, 18]);

// Use isEmpty function
$res = $collection->isEmpty();

// Display the result
var_dump($res);

// Create a collection
$collection = new \Ds\Vector();

// Use isEmpty function
$res = $collection->isEmpty();

// Display the result
var_dump($res);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a collection
$collection = new \Ds\Vector();

// display output
var_dump($collection->isEmpty());

// Create a collection
$collection = new \Ds\Vector([1, 3, 5, 2, 6]);

// Display output
var_dump($collection->isEmpty());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-collection.isempty.php](http://php.net/manual/en/ds-collection.isempty.php)
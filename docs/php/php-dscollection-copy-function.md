# PHP|ds\Collection copy()函数

> Original: [https://www.geeksforgeeks.org/php-dscollection-copy-function/](https://www.geeksforgeeks.org/php-dscollection-copy-function/)

Ds\Collection：：copy()函数是 PHP 中的一个内置函数，用于返回集合元素的副本。

**语法：**

```
Ds\Collection::copy ( void ) : Ds\Collection
```

**参数：**此函数不接受任何参数。

**返回值：**返回收集要素副本。

下面的程序说明了 PHP 中的 Ds\Collection：：Copy()函数：

**示例 1：**

```
<?php

// Create a collection
$collection = new \Ds\Vector([10, 15, 21, 13, 16, 18]);

// Display the collection element
print_r($collection);

// Use copy() function to remove elements
$collection->copy();

// Display the collection element
print_r($collection);

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a collection
$collection = new \Ds\Vector([10, 15, 21, 13, 16, 18]);

// Display the collection element
print_r($collection);

// Use copy() function to remove elements
$collection->copy();

// Pop an element from collection
$collection->pop();

// Display the collection element
print_r($collection);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-collection.copy.php](http://php.net/manual/en/ds-collection.copy.php)
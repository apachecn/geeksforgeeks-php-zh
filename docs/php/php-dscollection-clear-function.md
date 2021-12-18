# PHP|ds\Collection Clear()函数

> Original: [https://www.geeksforgeeks.org/php-dscollection-clear-function/](https://www.geeksforgeeks.org/php-dscollection-clear-function/)

Ds\Collection：：Clear()函数是 PHP 中的一个内置函数，用于从集合中删除所有值。

**语法：**

```
Ds\Collection::clear( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 ds\Collection：：Clear()函数：

**示例 1：**

```
<?php

// Create a collection
$collection = new \Ds\Vector([1, 2, 3, 4, 5, 6]);

// Display the collection element
print_r($collection);

// Use clear() function to remove elements
$collection->clear();

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
var_dump($collection);

// Use clear() function to remove elements
$collection->clear();

// Display the collection element
var_dump($collection);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-collection.clear.php](http://php.net/manual/en/ds-collection.clear.php)
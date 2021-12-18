# PHP|ds\Collection toArray()函数

> Original: [https://www.geeksforgeeks.org/php-dscollection-toarray-function/](https://www.geeksforgeeks.org/php-dscollection-toarray-function/)

Ds\Collection：：toArray()函数是 PHP 中的一个内置函数，用于将集合转换为数组。

**语法：**

```
*public* Ds\Collection::toArray( void ) : array
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含所有集合元素的数组。

以下程序说明了 PHP 中的公共 ds\Collection：：toArray()函数：

**示例 1：**

```
<?php 

// Create a collection 
$collection = new \Ds\Vector([10, 15, 21, 13, 16, 18]); 

// Use toArray() function to convert
// collections to array
var_dump($collection->toArray()); 

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

// Use toArray() function to convert 
// collection into array and print it
print_r($collection->toArray()); 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-collection.toarray.php](http://php.net/manual/en/ds-collection.toarray.php)
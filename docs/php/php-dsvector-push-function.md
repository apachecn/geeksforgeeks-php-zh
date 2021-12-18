# PHP|ds\Vector ush()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-push-function/](https://www.geeksforgeeks.org/php-dsvector-push-function/)

**Ds\Vector：：Push()**函数是 PHP 中的一个内置函数，用于将元素添加到向量的末尾。

**语法：**

```php
*void* public Ds\Vector::push( $values )

```

**参数：**此函数接受单个参数*$values*，该参数包含一个或多个要添加到向量中的元素。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Vector：：Push()**函数：

**程序 1：**

```php
<?php

// Create new vector
$arr1 = new \Ds\Vector([10, 20, 30, 40, 50]);

echo("Original vector elements\n");
print_r($arr1);

// Use push() function to add
// element to the vector
$arr1->push(60);

echo("\nVector after appending the elements\n");
print_r($arr1);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new vector
$arr1 = new \Ds\Vector([10, 20, 30, 40, 50]);

echo("Original vector elements\n");
print_r($arr1);

// Use push() function to add
// element to the vector
$arr1->push(...[60, 70]);

echo("\nVector after appending the elements\n");
print_r($arr1);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.push.php](http://php.net/manual/en/ds-vector.push.php)
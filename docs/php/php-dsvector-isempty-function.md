# PHP|ds\Vector isEmpty()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-isempty-function/](https://www.geeksforgeeks.org/php-dsvector-isempty-function/)

**ds\Vector：：isEmpty()**函数是 PHP 中的一个内置函数，用于检查向量是否为空。

**语法：**

```php
*bool* public Ds\Vector::isEmpty( void )

```

**参数：**此函数不接受任何参数。

**返回值：**如果向量为空，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**ds\Vector：：isEmpty()**函数：

**程序 1：**

```php
<?php

// Create new vector
$vector = new \Ds\Vector([1, 2, 4, 5]);

// Use isEmpty() function to
// check vector
var_dump($vector->isEmpty());

// Use clear() function to remove
// vector elements
$vector->clear();

// Use isEmpty() function
var_dump($vector->isEmpty());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new vector
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

// Use isEmpty() function to
// check vector
var_dump($vector->isEmpty());

// Use clear() function to remove
// vector elements
$vector->clear();

// Use isEmpty() function
var_dump($vector->isEmpty());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.isempty.php](http://php.net/manual/en/ds-vector.isempty.php)
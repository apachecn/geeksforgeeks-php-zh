# PHP|ds\Vector Apply()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-apply-function/](https://www.geeksforgeeks.org/php-dsvector-apply-function/)

**ds\Vector：：Apply()**函数是 PHP 中的一个内置函数，用于通过将回调函数应用于向量的每个值来更新数组中的所有值。 在此回调之后，向量的所有值都将按照回调函数中的定义进行修改。

**语法：**

```php
*void* public Ds\Vector::apply( $callback )

```

**参数：**此函数接受单个参数*$callback*，该参数用于更新向量中的值。 此回调函数应返回要替换向量元素的值。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Vector：：Apply()**函数：

**程序 1：**

```php
<?php

// Declare the callback function
$callback = function($value) {
    return $value / 10; 
};

// Declare a vector
$vector = new \Ds\Vector([10, 20, 30, 40, 50]);

// Use apply() function to call function
$vector->apply($callback);

// Display the vector element
print_r($vector);
?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declare the callback function
$callback = function($value) {
    return $value * 5;
};

// Declare a vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Use apply() function to call function
$vector->apply($callback);

// Display the vector element
print_r($vector);
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.apply.php](http://php.net/manual/en/ds-vector.apply.php)
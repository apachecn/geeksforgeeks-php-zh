# PHP|Ds\Vector Join()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-join-function/](https://www.geeksforgeeks.org/php-dsvector-join-function/)

**Ds\Vector：：Join()**函数是 PHP 中的一个内置函数，用于使用提供的分隔符作为参数将向量的所有元素连接为一个字符串。

**语法：**

```
*string* public Ds\Vector::join( $glue )

```

**参数：**此函数接受单个参数*$glue*，该参数用于保存分隔符。 这是一个可选参数。

**返回值：**此函数以字符串形式返回向量值。

以下程序说明了 PHP 中的**ds\Vector：：Join()**函数：

**程序 1：**

```
<?php

// Create new vector
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

// Display the vector element
print_r($vector);

echo("\nVector elements after joining\n");

print_r($vector->join());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new vector
$vector = new \Ds\Vector(["geeks", "for", "geeks"]);

// Display the vector element
print_r($vector);

echo("\nVector elements after joining\n");

print_r($vector->join("|"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.join.php](http://php.net/manual/en/ds-vector.join.php)
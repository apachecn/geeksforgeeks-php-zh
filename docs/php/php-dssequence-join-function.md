# PHP|ds\Sequence Join()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-join-function/](https://www.geeksforgeeks.org/php-dssequence-join-function/)

**Ds\Sequence：：Join()**函数是 PHP 中的一个内置函数，用于将所有值连接为字符串。

**语法：**

```php
*string* abstract public Ds\Sequence::join ([ string $glue ] )

```

**参数：**此函数接受可选的单个参数*$glue*。 它用于分隔序列元素。

**返回值：**此函数返回字符串。

以下程序说明了 PHP 中的**ds\Sequence：：Join()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector(["G", "E", "E",
                "K", "S", 1, 2, 3, 4]);

// Use join() function and
// display the string
var_dump($seq->join());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector(["G", "E", "E",
                "K", "S", 1, 2, 3, 4]);

// Use join() function and
// display the string separated
// with comma
var_dump($seq->join(", "));

// Create new sequence
$seq =  new \Ds\Vector([1, 2, 3, "g", "e"]);

// Use join() function
var_dump($seq->join("|"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.join.php](http://php.net/manual/en/ds-sequence.join.php)
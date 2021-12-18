# PHP|ds\Sequence get()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-get-function/](https://www.geeksforgeeks.org/php-dssequence-get-function/)

**Ds\Sequence：：Get()**函数是 PHP 中的一个内置函数，它返回给定索引处的值。

**语法：**

```php
*mixed* abstract public Ds\Sequence::get ( int $index )

```

**参数：**此函数接受单个参数*$index*，该参数保存访问元素的索引。

**返回值：**此函数返回给定索引处的值。

以下程序说明了 PHP 中的**ds\Sequence：：Get()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector(["G", "E", "E",
        "K", "S", "1", "2", 1, 2, 3, 4]);

// Use get() function
var_dump($seq->get(0));

// Use get() function
var_dump($seq->get(1));

// Use get() function
var_dump($seq->get(10));

// Use get() function
var_dump($seq->get(5));

// Use get() function
var_dump($seq->get(7));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector(["G", "E", "E",
        "K", "S", "1", "2", 1, 2, 3, 4]);

// Declare an index array
$arr = array (0, 1, 4, 6, 8, 5);

// Loop run for every array element  
foreach ($arr as $val) {  

    // Use get() function
    var_dump($seq->get($val));
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.get.php](http://php.net/manual/en/ds-sequence.get.php)
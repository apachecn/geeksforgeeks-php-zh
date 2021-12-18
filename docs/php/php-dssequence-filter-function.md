# PHP|ds\Sequence Filter()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-filter-function/](https://www.geeksforgeeks.org/php-dssequence-filter-function/)

**Ds\Sequence：：Filter()**函数是 PHP 中的一个内置函数，用于使用 Filter 函数创建新序列。

**语法：**

```
*Ds\Sequence* abstract public Ds\Sequence::filter ([ callable $callback ] )

```

**参数：**它是一个可选参数，如果应该包括该值，则返回 True，否则返回 False。

**返回值：**此函数返回一个新序列，其中包含回调返回 True 的所有值，如果未提供回调，则包含转换为 True 的所有值。

以下程序说明了 PHP 中的**ds\Sequence：：Filter()**函数：

**示例 1：**

```
<?php

// Create new sequence
$seq = new \Ds\Vector([10, 20, 30, 40, 50]);

// Display new sequence using filter function
var_dump($seq->filter(function($val) {
    return $val % 4 == 0;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create new sequence
$seq = new \Ds\Vector([2, 5, 4, 8, 3, 9]);

// Display new sequence using filter function
var_dump($seq->filter(function($val) {
    return $val;
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.filter.php](http://php.net/manual/en/ds-sequence.filter.php)
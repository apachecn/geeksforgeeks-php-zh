# PHP|ds\Sequence sum()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-sum-function/](https://www.geeksforgeeks.org/php-dssequence-sum-function/)

**Ds\Sequence：：sum()**函数是 PHP 中的一个内置函数，用于返回序列的所有值的总和。

**语法：**

```
*number* abstract public Ds\Sequence::sum( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数以整数或浮点数的形式返回所有序列元素的总和。

以下程序说明了 PHP 中的**ds\Sequence：：sum()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([5, 7, 8, 14, 23]);

// Use sum() function to find 
// the sum of sequence element
var_dump($seq->sum());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([5, 7.5, 8.4, 14, 23]);

// Use sum() function to find 
// the sum of sequence element
var_dump($seq->sum());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.sum.php](http://php.net/manual/en/ds-sequence.sum.php)
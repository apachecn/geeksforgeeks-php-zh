# PHP|ds\Sequence Merge()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-merge-function/](https://www.geeksforgeeks.org/php-dssequence-merge-function/)

Ds\Sequence：：Merge()函数是 PHP 中的一个内置函数，它在将所有给定值添加到序列之后返回序列。

**语法：**

```php
*abstract public* Ds\Sequence::merge( $values ) : Ds\Sequence
```

**参数：**此函数接受包含元素的单个参数*$values*。

**返回值：**此函数返回所有元素相加的序列。

下面的程序说明了 PHP 中的 Ds\Sequence：：Merge()函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

// Merge the sequence and display it
var_dump($seq->merge([1, 2, 3]));

// Display the sequence element
var_dump($seq)
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

// Merge the sequence and display it
var_dump($seq->merge(["G", "E", "E", "k", "S"]));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.merge.php](http://php.net/manual/en/ds-sequence.merge.php)
# PHP|ds\Sequence Sorted()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-sorted-function/](https://www.geeksforgeeks.org/php-dssequence-sorted-function/)

**Ds\Sequence：：Sorted()**函数是 PHP 中的一个内置函数，用于返回 Sequence 元素的排序副本。

**语法：**

```
*Ds\Sequence* abstract public Ds\Sequence::sorted( $comparator )
```

**参数：**此函数接受保存比较函数的单个参数*$compator*。 COMPARY 函数返回小于或大于等于零的整数值。

**返回值：**此函数返回序列的排序副本。

下面的程序说明了 PHP 中的**ds\Sequence：：Sorted()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([2, 4, 1, 9, 6, 5, 12, 9]);

// Use sorted() function to sort
// the sequence element
print_r($seq->sorted());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector(["Geeks", "GFG", "Abc", "for"]);

// Use sorted() function to sort
// the sequence element
print_r($seq->sorted());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.sorted.php](http://php.net/manual/en/ds-sequence.sorted.php)
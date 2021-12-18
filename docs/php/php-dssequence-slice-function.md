# PHP|ds\Sequence Slice()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-slice-function/](https://www.geeksforgeeks.org/php-dssequence-slice-function/)

**Ds\Sequence：：Slice()**函数是 PHP 中的一个内置函数，用于返回给定范围的子序列。

**语法：**

```
*Ds\Sequence* abstract public Ds\Sequence::slice ( int $index 
[, int $length ] )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$index:** this parameter saves the starting index of the subsequence. The indicator value can be positive or negative. If the index value is positive, it starts at the index of the sequence, and if the index value is negative, the sequence starts at the end.
*   **$Length:** this parameter saves the length of the subsequence. This parameter can take positive and negative values. If the length is positive, the size of the subsequence is equal to the given length, and if the length is negative, the sequence stops so many values from the end.

**返回值：**此函数返回给定范围的子序列。

下面的程序说明了 PHP 中的**ds\Sequence：：Slice()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([1, 3, 6, 9, 10, 15, 20]);

// Use slice() function to create 
// sub sequence and display it
print_r($seq->slice(2));

print_r($seq->slice(1, 2));

print_r($seq->slice(2, -2));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector(["Geeks", "GFG", "Abc", "for"]);

// Use slice() function to create 
// sub sequence and display it
print_r($seq->slice(3));

print_r($seq->slice(2, 0));

print_r($seq->slice(0, 3));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.slice.php](http://php.net/manual/en/ds-sequence.slice.php)
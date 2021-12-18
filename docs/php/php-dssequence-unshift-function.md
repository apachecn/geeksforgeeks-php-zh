# PHP|ds\Sequence unShift()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-unshift-function/](https://www.geeksforgeeks.org/php-dssequence-unshift-function/)

**Ds\Sequence：：UnShift()**函数是 PHP 中的一个内置函数，用于将值添加到序列的字体中。

**语法：**

```
*void* abstract public Ds\Sequence::unshift( $values )
```

**参数：**此函数接受单个参数*$values*，该参数包含要以序列字体添加的值。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Sequence：：UnShift()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

// Use unshift() function to 
// the sequence element
$seq->unshift("Geeks");

$seq->unshift("1", 1);

print_r($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector(["Geeks", "for", "Geeks"]);

// Use unshift() function to 
// the sequence element
$seq->unshift(1);

$seq->unshift("G", 10);

var_dump($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.unshift.php](http://php.net/manual/en/ds-sequence.unshift.php)
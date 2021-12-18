# PHP|DS\SEQUENCE CONTAINS()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-contains-function/](https://www.geeksforgeeks.org/php-dssequence-contains-function/)

**DS\SEQUENCE：：CONTAINS()**函数是 PHP 中的一个内置函数，用于检查序列中是否存在给定值。

**语法：**

```
*bool* abstract public Ds\Sequence::contains ([ mixed $...values ] )

```

**参数：**此函数接受单个或多个值，这些值需要检查序列中是否存在值。

**返回值：**如果序列中存在值，则返回 True，否则返回 False。

下面的程序说明了 PHP 中的**ds\Sequence：：CONTAINS()**函数：

**程序 1：**

```
<?php 

// Create a sequence 
$seq = new \Ds\Vector(['G', 'e', 'e', 'k', 's', 5, 2, 7]);

// Use contains() function to check elements
// exist in the sequence or not
var_dump($seq->contains('G')); 

var_dump($seq->contains('k'));

var_dump($seq->contains('p')); 

var_dump($seq->contains(7)); 

var_dump($seq->contains('5')); 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php 

// Create a sequence 
$seq = new \Ds\Vector(['G', 'e', 'e', 'k', 's', 5, 2, 7]);

// Use contains() function to check elements
// exist in the sequence or not
var_dump($seq->contains('G', 'e')); 

var_dump($seq->contains('k', 'e', 7));

var_dump($seq->contains('p', '1')); 

var_dump($seq->contains(7, 1)); 

var_dump($seq->contains('5', 5)); 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.contains.php](http://php.net/manual/en/ds-sequence.contains.php)
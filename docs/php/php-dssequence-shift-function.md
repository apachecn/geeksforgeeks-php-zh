# PHP|ds\Sequence Shift()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-shift-function/](https://www.geeksforgeeks.org/php-dssequence-shift-function/)

**Ds\Sequence：：Shift()**函数是 PHP 中的一个内置函数，用于从序列中删除第一个元素并返回它。

**语法：**

```
*mixed* abstract public Ds\Sequence::shift ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回从序列中删除的第一个值。

以下程序说明了 PHP 中的**ds\Sequence：：Shift()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([9, 10, 15, 20]);

// Use shift() function to remove
// first element from sequence
var_dump($seq->shift());

var_dump($seq->shift());

var_dump($seq->shift());

var_dump($seq->shift());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector(["Geeks", "for", "Geeks"]);

// Use shift() function to remove
// first element from sequence
var_dump($seq->shift());

var_dump($seq->shift());

var_dump($seq->shift());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.shift.php](http://php.net/manual/en/ds-sequence.shift.php)
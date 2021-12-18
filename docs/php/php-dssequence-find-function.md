# PHP|ds\Sequence find()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-find-function/](https://www.geeksforgeeks.org/php-dssequence-find-function/)

**Ds\Sequence：：find()**函数是 PHP 中的一个内置函数，用于从序列中查找值。 如果序列中存在值，则返回其索引值，否则返回 False。

**语法：**

```
*mixed* abstract public Ds\Sequence::find ( mixed $value ) 

```

**参数：**此函数接受单个参数*$value*，该参数需要检查它是否出现在序列中。

**返回值：**此函数成功时返回值的索引，失败时返回值的索引。

以下程序说明了 PHP 中的**ds\Sequence：：Find()**函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([21, 23, "p", "x"]);

// Use find() function
var_dump($seq->find("G"));

// Use find() function
var_dump($seq->find(21));

// Use find() function
var_dump($seq->find(10));

// Use find() function
var_dump($seq->find("x"));

// Use find() function
var_dump($seq->find("p"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector(["G", "E", "E",
        "K", "S", "1", "2", 1, 2, 3, 4]);

// Use find() function
var_dump($seq->find("G"));

// Use find() function
var_dump($seq->find(1));

// Use find() function
var_dump($seq->find(10));

// Use find() function
var_dump($seq->find("1"));

// Use find() function
var_dump($seq->find("k"));

// Use find() function
var_dump($seq->find("F"));

// Use find() function
var_dump($seq->find("4"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.find.php](http://php.net/manual/en/ds-sequence.find.php)
# PHP|ds\Sequence last()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-last-function/](https://www.geeksforgeeks.org/php-dssequence-last-function/)

**Ds\Sequence：：last()**函数是 PHP 中的一个内置函数，用于返回序列中的最后一个元素。

**语法：**

```php
*mixed* abstract public Ds\Sequence::last( void ) 
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回序列中的最后一个元素。

以下程序说明了 PHP 中的**ds\Sequence：：last()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([10, 20, 13, 25]);

// Display the last element from the sequence
var_dump($seq->last());

// Create new sequence
$seq =  new \Ds\Vector(['G', 'e', 'e', 'k', 's']);

// Display the last element from the sequence
var_dump($seq->last());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([21, 23, "p", "x"]);

// Display the last element
// from the sequence
var_dump($seq->last());

// Function to push an element
$seq->insert(4, "G");   

// Display the last element
// from the sequence
var_dump($seq->last());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.last.php](http://php.net/manual/en/ds-sequence.last.php)
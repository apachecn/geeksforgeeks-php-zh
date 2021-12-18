# PHP|ds\Sequence First()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-first-function/](https://www.geeksforgeeks.org/php-dssequence-first-function/)

**Ds\Sequence：：first()**函数是 PHP 中的一个内置函数，用于返回序列中的第一个元素。

**语法：**

```php
*mixed* abstract public Ds\Sequence::first ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回序列中的第一个元素。

下面的程序说明了 PHP 中的**ds\Sequence：：First()**函数：

**示例 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([10, 20, 13, 25]);

// Display the first element from the sequence
var_dump($seq->first());

// Create new sequence
$seq =  new \Ds\Vector(['G', 'e', 'e', 'k', 's']);

// Display the first element from the sequence
var_dump($seq->first());

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([21, 23, 'p', 'x']);

// Display the first element
// from the sequence
var_dump($seq->first());

// Function to push an element
$seq->insert(0, "G");   

// Display the first element
// from the sequence
var_dump($seq->first());

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.first.php](http://php.net/manual/en/ds-sequence.first.php)
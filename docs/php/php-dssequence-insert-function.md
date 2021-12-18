# PHP|ds\Sequence Insert()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-insert-function/](https://www.geeksforgeeks.org/php-dssequence-insert-function/)

**Ds\Sequence：：Insert()**函数是 PHP 中的一个内置函数，用于在序列中的给定索引处插入值。

**语法：**

```php
*void* abstract public Ds\Sequence::insert ( int $index [, mixed $...values ] )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$index:** this parameter holds the index value of where the element is inserted. Its value is between 0 < = $index < = count. Where COUNT represents the number of elements in the sequence.
*   **$VALUES:** this parameter holds the value to be inserted.

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Sequence：：Insert()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq = new \Ds\Vector();

// Use insert() function
$seq->insert(0, "g");

// Use insert() function
$seq->insert(1, "e");

// Use insert() function
$seq->insert(2, "e");

// Use insert() function
$seq->insert(3, "k");

// Use insert() function
$seq->insert(4, "s");

// Use insert() function
$seq->insert(5, 4);

var_dump($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq = new \Ds\Vector();

// Use insert() function to insert
// element in the sequence
$seq->insert(0, 1, 2, 3, 4, 5, 
    ["g", "e", "e", "k", 1, 2]);

var_dump($seq);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.insert.php](http://php.net/manual/en/ds-sequence.insert.php)
# PHP|ds\Sequence Push()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-push-function/](https://www.geeksforgeeks.org/php-dssequence-push-function/)

**Ds\Sequence：：Push()**函数是 PHP 中的一个内置函数，它将值添加到序列的末尾。

**语法：**

```php
*void* abstract public Ds\Sequence::push( $values )
```

**参数：**此函数接受包含一个或多个值的单个参数*$values*。 它保存要在序列中添加的值。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Sequence：：Push()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

// Use push() function to add
// element in the sequence
$seq->push(24);

// Use push() function to add
// element in the sequence
$seq->push("S");

// Use push() function to add
// element in the sequence
$seq->push("Geeks");

// Use push() function to add
// element in the sequence
$seq->push(2);

var_dump($seq);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

$arr = array ("g", "e", "e", "k");

// Loop run for every array element  
foreach ($arr as $val) {  

    // Use push() function to add
    // element in the sequence
    $seq->push($val);
}

var_dump($seq);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.push.php](http://php.net/manual/en/ds-sequence.push.php)
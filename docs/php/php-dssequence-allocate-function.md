# PHP|DS\SEQUENCE ALLOCATE()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-allocate-function/](https://www.geeksforgeeks.org/php-dssequence-allocate-function/)

**DS\SEQUENCE：：ALLOCATE()**函数是 PHP 中的一个内置函数，用于为所需的容量分配足够的内存。

**语法：**

```php
*void* abstract public Ds\Sequence::allocate ( int $capacity )

```

**参数：**此函数接受单个参数*$Capacity*，该参数表示分配的容量数量。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Sequence：：Allocation()**函数：

**示例 1：**

```php
<?php

// Create new sequence
$seq = new \Ds\Vector();

// Use capacity() function to 
// display the capacity
var_dump($seq->capacity());

// Allocate capacity
$seq->allocate(50);

// Display capacity
var_dump($seq->capacity());

// Allocate capacity
$seq->allocate(80);

// Display capacity
var_dump($seq->capacity());
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create new sequence
$seq = new \Ds\Vector();

// Declare capacity array
$arr = array(10, 20, 30, 40);

// Loop run for every array element  
foreach ($arr as $val) {  

    // Allocate capacity
    $seq->allocate($val);

    // Display capacity
    var_dump($seq->capacity());
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.allocate.php](http://php.net/manual/en/ds-sequence.allocate.php)
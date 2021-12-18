# PHP|ds\Sequence Apply()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-apply-function/](https://www.geeksforgeeks.org/php-dssequence-apply-function/)

**Ds\Sequence：：Apply()**函数是 PHP 中的一个内置函数，用于通过对每个值应用回调函数来更新 Sequence 的所有值。

**语法：**

```php
*void* abstract public Ds\Sequence::apply ( callable $callback )

```

**参数：**此函数接受单个参数**$callback**，该参数用于应用于序列中的每个值。

**返回值：**此函数不返回任何参数。

以下程序说明了 PHP 中的**ds\Sequence：：Apply()**函数：

**程序 1：**

```php
<?php 

// Create new sequence 
$seq = new \Ds\Vector([10, 20, 30, 40, 50]); 

// Use apply() function
$seq->apply(function($val) { 
    return $val / 5; 
}); 

// Display result
print_r($seq);

?> 
```

**输出：**

```php
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
    [3] => 8
    [4] => 10
)

```

**程序 2：**

```php
<?php 

// Create new sequence 
$seq = new \Ds\Vector([2, 3, 5, 6, 8]); 

// Use apply() function
$seq->apply(function($val) { 
    return $val; 
}); 

// Display result
var_dump($seq);

?> 
```

**输出：**

```php
object(Ds\Vector)#1 (5) {
  [0]=>
  int(2)
  [1]=>
  int(3)
  [2]=>
  int(5)
  [3]=>
  int(6)
  [4]=>
  int(8)
}

```

**引用：**[https://www.php.net/manual/en/ds-sequence.apply.php](https://www.php.net/manual/en/ds-sequence.apply.php)
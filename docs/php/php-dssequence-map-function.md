# PHP|ds\Sequence map()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-map-function/](https://www.geeksforgeeks.org/php-dssequence-map-function/)

**Ds\Sequence：：Map()**函数是 PHP 中的一个内置函数，它在对每个值应用回调函数后返回结果。

**语法：**

```php
*Ds\Sequence* abstract public Ds\Sequence::map( $callback )
```

**参数：**此函数接受单个参数$callback。 回调应用于 Sequence 的每个值。

**返回值：**此函数在应用每个值后返回回调。

以下程序说明了 PHP 中的**ds\Sequence：：Map()**函数：

**程序 1：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector( [4, 8, 12, 16] );

// Use map() function and display it
var_dump($seq->map(function($val) { 
        return $val * 3; 
}));

?>
```

```php
Output:
object(Ds\Vector)#3 (4) {
  [0]=>
  int(12)
  [1]=>
  int(24)
  [2]=>
  int(36)
  [3]=>
  int(48)
}
```

**程序 2：**

```php
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

// Use map() function and display it 
var_dump($seq->map(function($val) { 
        return $val / 3; 
}));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.map.php](http://php.net/manual/en/ds-sequence.map.php)
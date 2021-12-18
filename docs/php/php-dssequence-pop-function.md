# PHP|ds\Sequence POP()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-pop-function/](https://www.geeksforgeeks.org/php-dssequence-pop-function/)

Ds\Sequence：：op()函数是 PHP 中的一个内置函数，它从 Sequence 中删除最后一个值并返回它。

**语法：**

```
*abstract public* Ds\Sequence::pop( void ) : mixed
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回弹出的值。

下面的程序说明了 PHP 中的 Ds\Sequence：：POP()函数：

**程序 1：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector( [12, 15, 18, 20] );

// pop the sequence element
var_dump($seq->pop());

// pop the sequence element
var_dump($seq->pop());

// pop the sequence element
var_dump($seq->pop());

// pop the sequence element
var_dump($seq->pop());
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new sequence
$seq =  new \Ds\Vector([12, 15, 18, 20]);

for ($i = 0; $i < 4; $i++) {

    // Pop the sequence element
    var_dump($seq->pop());
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-sequence.pop.php](http://php.net/manual/en/ds-sequence.pop.php)
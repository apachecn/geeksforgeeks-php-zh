# PHP|ds\Sequence Capacity()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-capacity-function/](https://www.geeksforgeeks.org/php-dssequence-capacity-function/)

**Ds\Sequence：：Capacity()**函数是 PHP 中的内置函数，用于返回 Sequence 的当前容量。

**语法：**

```
*int* abstract public Ds\Sequence::capacity ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回序列的当前容量。

以下程序说明了 PHP 中的**ds\Sequence：：Capacity()**函数：

**程序 1：**

```
<?php

// Declare a sequence
$seq = new \Ds\Vector();

// Use capacity() function
var_dump($seq->capacity());

// Push element in sequence
$seq->push(...range(1, 100));

// Use capacity() function
var_dump($seq->capacity());

// Pop element in sequence
$seq->pop();

// Use capacity() function
var_dump($seq->capacity());

?>
```

**输出：**

```
int(8)
int(100)
int(100)

```

**程序 2：**

```
<?php

// Declare a sequence
$seq = new \Ds\Vector();

// Push element in sequence
$seq->push(...range(1, 50));

// Use capacity() function
var_dump($seq->capacity());

// Push element in sequence
$seq->push(...range(1, 50));

// Use capacity() function
var_dump($seq->capacity());

?>
```

**输出：**

```
int(50)
int(100)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.capacity.php](https://www.php.net/manual/en/ds-sequence.capacity.php)
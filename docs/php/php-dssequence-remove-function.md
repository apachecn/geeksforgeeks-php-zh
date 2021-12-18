# PHP|ds\Sequence Remove()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-remove-function/](https://www.geeksforgeeks.org/php-dssequence-remove-function/)

**Ds\Sequence：：Remove()**函数是 PHP 中的一个内置函数，用于按索引删除和返回值。

**语法：**

```
*mixed* abstract public Ds\Sequence::remove ( int $index )

```

**参数：**此函数接受单个参数**$index**，该参数保存要删除的值的索引。

**返回值：**此函数返回删除的值。

以下程序说明了 PHP 中的**ds\Sequence：：Remove()**函数：

**程序 1：**

```
<?php

// Declare a sequence
$seq = new \Ds\Vector(["Geeks", "Hello", "GFG"]);

// Use remove() function
var_dump($seq->remove(2));
var_dump($seq->remove(0));

?>
```

**输出：**

```
string(3) "GFG"
string(5) "Geeks"

```

**程序 2：**

```
<?php

// Declare a sequence
$seq = new \Ds\Vector([1, 3, 5, 7, 8, 9]);

// Use remove() function
$seq->remove(5);
$seq->remove(3);
$seq->remove(2);
$seq->remove(0);

var_dump($seq->remove(1));

?>
```

**输出：**

```
int(8)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.remove.php](https://www.php.net/manual/en/ds-sequence.remove.php)
# PHP|ds\Sequence Rotate()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-rotate-function/](https://www.geeksforgeeks.org/php-dssequence-rotate-function/)

**Ds\Sequence：：Rotate()**函数是 PHP 中的一个内置函数，用于将序列元素旋转给定的旋转次数。

**语法：**

```
*void* abstract public Ds\Sequence::rotate ( int $rotations )

```

**参数：**此函数接受保存旋转次数的单个参数**$rotation**。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**ds\Sequence：：Rotate()**函数：

**程序 1：**

```
<?php 

// Create new Sequence
$seq = new \Ds\Vector([1, 2, 3, 4, 5]); 

echo("Original Sequence\n"); 

// Display the Sequence elements 
print_r($seq); 

// Use rotate() function to rotate 
// the sequence elements 
$seq->rotate(3); 

echo("\nSequence after rotating by 3 places\n"); 

// Display the Sequence elements 
print_r($seq); 

?> 
```

**输出：**

```
Original Sequence
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)

Sequence after rotating by 3 places
Ds\Vector Object
(
    [0] => 4
    [1] => 5
    [2] => 1
    [3] => 2
    [4] => 3
)

```

**程序 2：**

```
<?php 

// Create new Sequence
$seq = new \Ds\Vector(["Geeks", "for", "Geeks", 
        "Computer", "Science", "Portal"]); 

echo("Original Sequence\n"); 

// Display the Sequence elements 
print_r($seq); 

// Use rotate() function to rotate 
// the sequence elements 
$seq->rotate(8); 

echo("\nSequence after rotating by 8 places\n"); 

// Display the Sequence elements 
print_r($seq); 

?> 
```

**输出：**

```
Original Sequence
Ds\Vector Object
(
    [0] => Geeks
    [1] => for
    [2] => Geeks
    [3] => Computer
    [4] => Science
    [5] => Portal
)

Sequence after rotating by 8 places
Ds\Vector Object
(
    [0] => Geeks
    [1] => Computer
    [2] => Science
    [3] => Portal
    [4] => Geeks
    [5] => for
)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.rotate.php](https://www.php.net/manual/en/ds-sequence.rotate.php)
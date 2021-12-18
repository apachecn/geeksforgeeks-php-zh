# PHP|ds\Sequence Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-reverse-function/](https://www.geeksforgeeks.org/php-dssequence-reverse-function/)

**Ds\Sequence：：Reverse()**函数是 PHP 中的一个内置函数，用于就地反转序列。

**语法：**

```
*void* abstract public Ds\Sequence::reverse ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Sequence：：Reverse()**函数：

**程序 1：**

```
<?php 

// Create new Vector 
$seq = new \Ds\Vector([1, 2, 3, 4, 5]); 

// Display the elements 
print_r($seq); 

echo("Sequence after reversing\n"); 

// Use reverse() function to reverse 
// the element and display it 
$seq->reverse();

print_r($seq);

?>
```

**输出：**

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
Sequence after reversing
Ds\Vector Object
(
    [0] => 5
    [1] => 4
    [2] => 3
    [3] => 2
    [4] => 1
)

```

**程序 2：**

```
<?php 

// Create new Vector 
$seq = new \Ds\Vector(["Geeks", "for", "Geeks",
        "Computer", "Science", "Portal"]); 

// Display the elements 
print_r($seq); 

echo("Sequence after reversing\n"); 

// Use reverse() function to reverse 
// the element and display it 
$seq->reverse();

print_r($seq);

?>
```

**输出：**

```
Ds\Vector Object
(
    [0] => Geeks
    [1] => for
    [2] => Geeks
    [3] => Computer
    [4] => Science
    [5] => Portal
)
Sequence after reversing
Ds\Vector Object
(
    [0] => Portal
    [1] => Science
    [2] => Computer
    [3] => Geeks
    [4] => for
    [5] => Geeks
)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.reverse.php](https://www.php.net/manual/en/ds-sequence.reverse.php)
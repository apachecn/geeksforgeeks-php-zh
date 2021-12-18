# PHP|ds\Sequence Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-reversed-function/](https://www.geeksforgeeks.org/php-dssequence-reversed-function/)

**Ds\Sequence：：Reverse()**函数是 PHP 中的一个内置函数，用于返回 Sequence 元素的反向副本。

**语法：**

```php
*Ds\Sequence* abstract public Ds\Sequence::reversed ( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Sequence 元素的反转副本。

以下程序说明了 PHP 中的**ds\Sequence：：Reverse()**函数：

**程序 1：**

```php
<?php 

// Create new Sequence 
$seq = new \Ds\Vector([1, 2, 3, 4, 5]); 

// Display the sequence elements 
print_r($seq); 

echo("After reversing the sequence elements\n"); 

// Use reversed() function to reverse 
// the copy of sequence and display it 
print_r($seq->reversed()); 

?> 
```

**输出：**

```php
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
After reversing the sequence elements
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

```php
<?php 

// Create new Vector 
$seq = new \Ds\Vector(["Geeks", "for", "Geeks",
        "Computer", "Science", "Portal"]); 

// Display the elements 
print_r($seq); 

echo("Sequence after reversing\n"); 

// Use reversed() function to reverse 
// the element and display it 
print_r($seq->reversed());

?>
```

**输出：**

```php
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

**引用：**[https://www.php.net/manual/en/ds-sequence.reversed.php](https://www.php.net/manual/en/ds-sequence.reversed.php)
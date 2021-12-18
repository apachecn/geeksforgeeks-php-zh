# PHP|ds\Sequence Set()函数

> Original: [https://www.geeksforgeeks.org/php-dssequence-set-function/](https://www.geeksforgeeks.org/php-dssequence-set-function/)

**Ds\Sequence：：Set()**函数是 PHP 中的一个内置函数，用于更新给定索引处的值。

**语法：**

```php
*void* abstract public Ds\Sequence::set ( int $index , mixed $value )

```

**参数：**此函数接受上述两个参数：

*   **$index:** it is used to save the index number of the sequence value to be updated.
*   **$VALUE:** is used to save the new value updated at the given index.

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Sequence：：Set()**函数：

**程序 1：**

```php
<?php 

// Create new Sequence
$seq = new \Ds\Vector([1, 2, 3, 4, 5]); 

echo("Original Sequence\n"); 

// Display the Sequence elements 
print_r($seq); 

// Use set() function to update
// the sequence elements 
$seq->set(2, "Geeks");

echo("\nSequence after updating the elements\n"); 

// Display the Sequence elements 
print_r($seq); 

?> 
```

**输出：**

```php
Original Sequence
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)

Sequence after updating the elements
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => Geeks
    [3] => 4
    [4] => 5
)

```

**程序 2：**

```php
<?php 

// Create new Sequence
$seq = new \Ds\Vector(["Geeks", "for", "Geeks", 
        "Computer", "Science", "Portal"]); 

echo("Original Sequence\n"); 

// Display the Sequence elements 
print_r($seq); 

// Use set() function to set
// the sequence elements 
$seq->set(0, "Welcome");
$seq->set(1, "to");
$seq->set(2, "GeeksforGeeks");

echo("\nSequence after updating the elements\n"); 

// Display the Sequence elements 
print_r($seq); 

?> 
```

**输出：**

```php
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

Sequence after updating the elements
Ds\Vector Object
(
    [0] => Welcome
    [1] => to
    [2] => GeeksforGeeks
    [3] => Computer
    [4] => Science
    [5] => Portal
)

```

**引用：**[https://www.php.net/manual/en/ds-sequence.set.php](https://www.php.net/manual/en/ds-sequence.set.php)
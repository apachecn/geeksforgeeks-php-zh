# PHP|ds\Vector Reverse()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-reverse-function/](https://www.geeksforgeeks.org/php-dsvector-reverse-function/)

**ds\Vector：：Reverse()**函数是 PHP 中的一个内置函数，用于就地反转向量元素。

**语法：**

```php
*void* public Ds\Vector::reverse( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**ds\Vector：：Reverse()**函数：

**程序 1：**

```php
<?php 

// Create new Vector 
$arr = new \Ds\Vector([1, 2, 3, 4, 5]); 

// Display the elements 
print_r($arr); 

echo("Vector after reversing\n"); 

// Use reverse() function to reverse 
// the vector elements and display it 
$arr->reverse();

print_r($arr);

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
Vector after reversing
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
$arr = new \Ds\Vector(["Geeks", "GFG",
        "Computer", "Science", "Portal"]); 

// Display the elements 
print_r($arr); 

echo("Vector after reversing\n"); 

// Use reverse() function to reverse 
// the vector elements and display it 
$arr->reverse();

print_r($arr);

?>
```

**输出：**

```php
Ds\Vector Object
(
    [0] => Geeks
    [1] => GFG
    [2] => Computer
    [3] => Science
    [4] => Portal
)
Vector after reversing
Ds\Vector Object
(
    [0] => Portal
    [1] => Science
    [2] => Computer
    [3] => GFG
    [4] => Geeks
)

```

**引用：**[https://www.php.net/manual/en/ds-vector.reverse.php](https://www.php.net/manual/en/ds-vector.reverse.php)
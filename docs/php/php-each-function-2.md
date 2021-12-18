# PHP|Each()函数

> Original: [https://www.geeksforgeeks.org/php-each-function-2/](https://www.geeksforgeeks.org/php-each-function-2/)

Each()函数是 PHP 中的一个内置函数，它基本上返回一个包含四个元素的数组，其中两个元素(1 和 value)表示元素值，两个元素(0 和 key)表示元素键，并将光标向前移动。
**语法：**

```php
*each(array)*
```

**参数：**

```php
Array:
It specifies the array which is being 
taken as input and used for each() function.

```

**返回值：**

```php
It returns the current element key and value which are an array with four elements out of
which two elements (1 and Value) for the element value, and two elements (0 and Key) for 
the element key.It returns FALSE if there are no array elements.

```

**PHP 版本：**
4+
**让我们看看 PHP 程序：**
程序 1：

```php
<?php
// PHP program to demonstrate working of each()
// for simple array.

// input array contain some elements inside.
$a = array("Ram", "Shita", "Geeta");

// each() function return in the array with four elements
// Two elements (1 and Value) for the element value which 
// are Ram, and two elements (0 and Key) for the element
// key which are not given here so output is zero.
print_r (each($a));

// Next set is printed as cursor is moved
print_r (each($a));
?>
```

**Output:**

```php
Array
(
    [1] => Ram
    [value] => Ram
    [0] => 0
    [key] => 0
)
Array
(
    [1] => Shita
    [value] => Shita
    [0] => 1
    [key] => 1
)

```
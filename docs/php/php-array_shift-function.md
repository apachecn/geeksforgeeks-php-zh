# PHP | array_shift()函数

> 原文:[https://www.geeksforgeeks.org/php-array_shift-function/](https://www.geeksforgeeks.org/php-array_shift-function/)

PHP 的这个内置函数从数组中移除第一个元素，并返回被移除元素的值。删除第一个元素后，剩余元素的键将被修改，并从开始重新编号，仅当键是数字时。换句话说，这个函数基本上将数组中的一个元素从开始处移开。

**语法**:

```php
array_shift($array)
```

**参数:**函数只取一个参数， *$array* 指需要移位的原始输入数组。

**返回值:**如前所述，函数从数组中返回移位元素的值，否则如果数组为空，则返回 NULL。

**示例:**

```php
Input : $array = ("ram"=>2, "aakash"=>4, "saran"=>5, "mohan"=>100)
Output : 2

Input : $array = (45, 5, 1, 22, 22, 10, 10);
Output :45

```

在这个程序中，我们将看到这个函数在 key_value 对数组中是如何工作的。

```php
<?php
// PHP function to illustrate the use of array_shift()
function Shifting($array)
{
    print_r(array_shift($array));
    echo "\n";
    print_r($array);
}
$array = array("ram"=>2, "aakash"=>4, "saran"=>5, "mohan"=>100);
Shifting($array);
?>
```

输出:

```php
2
Array
(
    [aakash] => 4
    [saran] => 5
    [mohan] => 100
)
```

现在让我们看看函数是如何处理默认键的。

```php
<?php
// PHP function to illustrate the use of array_shift()
function Shifting($array)
{
    print_r(array_shift($array));
    echo "\n";
    print_r($array);
}
$array = array(45, 5, 1, 22, 22, 10, 10);
Shifting($array);
?>
```

输出:

```php
45
Array
(
    [0] => 5
    [1] => 1
    [2] => 22
    [3] => 22
    [4] => 10
    [5] => 10
)

```

**参考**:
T3】http://php.net/manual/en/function.array-shift.php
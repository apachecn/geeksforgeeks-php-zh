# PHP | array_pop()函数

> 原文:[https://www.geeksforgeeks.org/php-array_pop-function/](https://www.geeksforgeeks.org/php-array_pop-function/)

PHP 的这个内置函数用于删除或弹出并返回数组中作为参数传递给它的最后一个元素。由于从数组中移除了最后一个元素，因此它将数组的大小减少了一。

**语法**:

```
array_pop($array)
```

**参数:**该函数只取一个参数 *$array* ，即输入数组并从中弹出最后一个元素，大小减少一。

**返回值:**这个函数返回数组的最后一个元素。如果数组为空或者输入参数不是数组，则返回空值。

**注意:**该功能在使用后复位(reset())输入数组的数组指针。

示例:

```
Input : $array = (1=>"ram", 2=>"krishna", 3=>"aakash");
Output : aakash

Input : $array = (24, 48, 95, 100, 120);
Output : 120

```

下面的程序说明了 PHP 中的 array_pop()函数:

**例 1**

```
<?php
// PHP code to illustrate the use of array_pop()

$array = array(1=>"ram", 2=>"krishna", 3=>"aakash");

print_r("Popped element is ");
echo array_pop($array);

print_r("\nAfter popping the last element, ".
                "the array reduces to: \n");
print_r($array);
?>
```

输出:

```
Popped element is aakash
After popping the last element, the array reduces to: 
Array
(
    [1] => ram
    [2] => krishna
)

```

**例 2**

```
<?php
$arr = array(24, 48, 95, 100, 120);

print_r("Popped element is ");
echo array_pop($arr);

print_r("\nAfter popping the last element, ".
                "the array reduces to: \n");
print_r($arr);
?>
```

输出:

```
Popped element is 120
After popping the last element, the array reduces to: 
Array
(
    [0] => 24
    [1] => 48
    [2] => 95
    [3] => 10
)

```

**异常:**如果传递了非数组，则抛出 E_WARNING 异常，这是运行时错误或警告。此警告不会停止脚本的执行。

**参考**:
T3】http://php.net/manual/en/function.array-pop.php
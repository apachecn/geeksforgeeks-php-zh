# PHP | array_slice()函数

> 原文:[https://www.geeksforgeeks.org/php-array_slice-function/](https://www.geeksforgeeks.org/php-array_slice-function/)

array_slice()是 PHP 的一个内置函数，用于根据用户的选择，通过对数组进行切片来获取数组的一部分。
**语法**:

```
array_slice($array, $start_point, $slicing_range, preserve)
```

**参数:**这个函数可以取四个参数，描述如下:

1.  **$array(必选):**这个参数指的是原始数组，我们要切片。
2.  **$start_point(必选):**此参数是指需要执行切片的数组的起始位置。必须提供该值。如果提供的值为负，则函数从数组的末尾开始切片，即-1 表示数组的最后一个元素。
3.  **$slicing _range(可选):**该参数是指需要进行切片的范围或极限点。负值将指示从字符串末尾开始的计数。现在，这个也可以留空。如果留空，该函数将从起点到终点对所有值进行切分。
4.  **保留(可选):**该参数只能取两个布尔参数，即*真*或*假*。这将告诉该功能是保留按键还是重置按键。True 表示保留密钥，false 表示重置密钥。默认值为 False。

**返回值:**如前所述，该函数将返回数组的选定部分或切片部分。
下面的程序说明了 PHP 中的 array_slice()函数:

*   在这个程序中，我们将传递所有的正参数以及*真*值来保存密钥。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate the
// array_slice() function

// Input array
$array = array("ram", "krishna", "aakash",
                        "gaurav", "raghav");

// Slice from pos 1 to pos 3                       
print_r(array_slice($array, 1, 3, true));

?>
```

输出:

```
Array
(
    [1] => krishna
    [2] => aakash
    [3] => gaurav
)
```

*   现在让我们通过传递与上述程序中相同的值来观察输出，但是使用 *False* 作为保留键的值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate the
// array_slice() function

// input array
$array = array("ram", "krishna", "aakash",
                        "gaurav", "raghav");

// Slice from pos 1 to pos 3
print_r(array_slice($array, 1, 3, false));

?>
```

输出:

```
Array
(
    [0] => krishna
    [1] => aakash
    [2] => gaurav
)
```

*   下面的程序显示了当我们不给出范围参数时会发生什么:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate the
// use of array_slice()

// Input array
$array = array("ram", "krishna", "aakash",
                        "gaurav", "raghav");

// Slice from pos 1 to end
print_r(array_slice($array, 1));

?>
```

输出:

```
Array
(
    [0] => krishna
    [1] => aakash
    [2] => gaurav
    [3] => raghav
)
```

*   下面的程序说明了当我们传递负参数作为我们的起始位置时的 array_slice()函数:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate the
// use of array_slice()

// Input array
$array = array("ram", "krishna", "aakash",
                        "gaurav", "raghav");

// Slice from pos 3rd position to
// the end of the array
print_r(array_slice($array, -3));

?>
```

输出:

```
Array
(
    [0] => aakash
    [1] => gaurav
    [2] => raghav
)
```

*   下面的程序显示了当我们试图传递负参数作为起点和长度或范围时会发生什么:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// PHP program to illustrate the
// use of array_slice()

// Input Array
$array = array("ram", "krishna", "aakash",
                        "gaurav", "raghav");

// Slice from pos 1 to end
print_r(array_slice($array, -3, -2, true));

?>
```

输出:

```
Array
(
    [2] => aakash
)
```

**参考**:
T3】http://php.net/manual/en/function.array-slice.php
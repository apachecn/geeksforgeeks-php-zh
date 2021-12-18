# PHP | array_reduce()函数

> 原文:[https://www.geeksforgeeks.org/php-array_reduce-function/](https://www.geeksforgeeks.org/php-array_reduce-function/)

PHP 的这个内置函数用于将一个数组的元素简化为一个可以是浮点、整数或字符串值的单个值。该函数使用用户定义的回调函数来减少输入数组。

**语法**:

```php
array_reduce($array, own_function, $initial)
```

**参数:**
该函数采用三个参数，描述如下:

1.  **$array(必选):**这是一个必选参数，指的是我们需要从中进行约简的原始数组。
2.  **own_function(强制):**此参数也是强制的，指的是用于保存$array 值的用户定义函数
3.  **$initial(可选):**此参数为可选参数，指的是要发送给函数的值。

**返回值:**该函数返回缩小后的结果。它可以是任何类型的 int、float 或 string。

示例:

```php
Input : $array = (15, 120, 45, 78)
        $initial = 25
        own_function() takes two parameters and concatenates 
        them with "and" as a separator in between
Output : 25 and 15 and 120 and 45 and 78

Input : $array = array(2, 4, 5);
        $initial = 1
        own_function() takes two parameters 
        and multiplies them.
Output : 40
```

在这个程序中，我们将看到整数元素的数组是如何被简化为单个字符串值的。我们也通过了我们选择的初始元素。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP function to illustrate the use of array_reduce()
function own_function($element1, $element2)
{
    return $element1 . " and " . $element2;
}

$array = array(15, 120, 45, 78);
print_r(array_reduce($array, "own_function", "Initial"));
?>
```

**输出:**

```php
Initial and 15 and 120 and 45 and 78
```

在下面的程序中，array_reduce 使用 own_function()将给定的数组简化为数组所有元素的乘积。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP function to illustrate the use of array_reduce()
function own_function($element1, $element2)
{
    $element1 = $element1 * $element2;
    return $element1;
}

$array = array(2, 4, 5, 10, 100);
print_r(array_reduce($array, "own_function", "2"));
?>
```

**输出:**

```php
80000
```

**参考**:
T3】http://php.net/manual/en/function.array-reduce.phpT5】
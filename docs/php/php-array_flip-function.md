# PHP | array_flip()函数

> 原文:[https://www.geeksforgeeks.org/php-array_flip-function/](https://www.geeksforgeeks.org/php-array_flip-function/)

PHP 的这个内置函数用于交换数组中的元素，即交换数组中所有键及其相关值，反之亦然。我们必须记住，数组的值必须是有效的键，即它们必须是整数或字符串。如果值的类型错误，将引发警告，并且有问题的键/值对将不会包含在结果中。

**示例:**

```
Input : array = ("aakash" => 20, "rishav" => 40, "gaurav" => 60)
Output:
        Array
        (
          [20] => aakash
          [40] => rishav
          [60] => gaurav
        )
Explanation: The keys and values are exchanged and the last key or value is taken.

Input : array = ("aakash" => "rani", "rishav" => "sristi", 
                 "gaurav" => "riya", "laxman" => "rani")
Output:
        Array
        (
          [rani] => laxman
          [sristi] => rishav
          [riya] => gaurav
        )

```

**语法:**

```
*array* array_flip($array)
```

**参数:**该函数只取一个引用输入数组的参数 **$array** 。

**返回类型:**该函数返回另一个数组，元素交换或翻转后，如果输入数组无效，则返回 null。

下面的程序说明了 **array_flip()函数**在 PHP 中的工作:
**例 1:**

```
<?php

// PHP function to illustrate the use of array_flip()
function Flip($array)
{
    $result = array_flip($array);
    return($result);
}

$array = array("aakash" => "rani", "rishav" => "sristi", 
               "gaurav" => "riya", "laxman" => "rani");
print_r(Flip($array));

?>
```

**输出:**

```
Array
(
    [rani] => laxman
    [sristi] => rishav
    [riya] => gaurav
)

```

如果数组中的多个值相同，那么在使用 array_flip()函数时，只有索引最大的键(交换后)才会被添加到数组中。(这样做是为了确保没有重复的密钥。)

**例 2:**

```
<?php
// PHP program to array_flip() with multiple similar values

//function to use array_flip() 
function Flip($array)
{
    $result = array_flip($array);
    return($result);
}

//make the array
$array = array("a" => 1, "b" => 1, "c" => 2);

//print all resultant values
print_r(Flip($array)); 

?>
```

**输出:**

```
Array
(
    [1] => b
    [2] => c
)

```

**参考文献:**T2】http://php.net/manual/en/function.array-flip.php
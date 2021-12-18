# PHP|Shuffle()函数

> Original: [https://www.geeksforgeeks.org/php-shuffle-function/](https://www.geeksforgeeks.org/php-shuffle-function/)

Shuffle()函数是 PHP 中的一个内置函数，用于对数组中元素的顺序进行置乱或随机化。 此函数为数组中的元素分配新键。 它还将删除所有现有键，而不仅仅是重新排序键并从零开始分配数字键。

**语法：**

```php
*boolean* shuffle($array)
```

**参数：**此函数接受单个参数*$array*。 它指定了我们要混洗的数组。

**返回值：**此函数返回布尔值，即 True 或 False。 成功时返回 TRUE，失败时返回 FALSE。

**注意：**此函数适用于 PHP 版本 4+。

例如：

```php
Input:- array("a"=>"Ram", 
              "b"=>"Shita", 
              "c"=>"Geeta", 
              "d"=>"geeksforgeeks" )
Output:- array( [0] => Geeta,
                [1] => Shita,
                [2] => Ram,
                [3] => geeksforgeeks )
Explanation: Here as we can see that input contain elements 
             in a order but in output order become shuffled.
```

下面的程序演示了 PHP 中的 Shuffle()的工作原理：

*   当输入数组是关联数组时，则 Shuffle()函数将使元素的顺序随机化，并从零(0)开始为元素分配新的键。

## PHP

```php
<?php

// input array contain some elements which
// need to be shuffled.
$a = array
     ( 
        "a"=>"Ram",
        "b"=>"Shita",
        "c"=>"Geeta",
        "d"=>"geeksforgeeks"
     );

shuffle($a);
print_r($a);

?>
```

**输出：**

```php
Array
(
    [0] => geeksforgeeks
    [1] => Shita
    [2] => Ram
    [3] => Geeta
)
```

*   当输入数组不是关联数组时，则 shffle()函数会将顺序随机化，并将数组转换为键从零(0)开始的关联数组。

## PHP

```php
<?php

// input array contain some elements
// which need to be shuffled.
$a = array
     (
        "ram",
        "geeta",
        "blue",
        "red",
        "shyam"
     );

shuffle($a);
print_r($a);

?>
```

**输出：**

```php
Array
(
    [0] => red
    [1] => geeta
    [2] => ram
    [3] => shyam
    [4] => blue
)
```

**参考**：
[http://php.net/manual/en/function.shuffle.php](http://php.net/manual/en/function.shuffle.php)
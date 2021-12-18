# PHP|Each()函数

> Original: [https://www.geeksforgeeks.org/php-each-function/](https://www.geeksforgeeks.org/php-each-function/)

Each()函数是 PHP 中的一个内置函数，用于获取内部指针当前指向的给定数组的当前元素键-值对。 返回当前元素的键和值后，内部指针在数组中加 1。

**注意**：如果您想使用 Each()再次遍历数组，可以使用 Reset()函数。

**语法**：

```php
each($array)

```

**参数**：此函数接受单个参数*$array*，它是我们要在其中查找内部指针当前指向的当前键-值对的输入数组。

**返回值**：此函数返回输入数组*$array*的当前元素的键值对。 键-值对以包含四个元素的新数组的形式返回。 前两个带有键(1 和 value)的元素用于当前元素的值，后两个带有键(0 和 key)的元素用于当前元素的键。 如果输入数组为空，或者如果内部指针已到达数组末尾，则此函数返回 FALSE。

示例：

```php
Input : each(array('Ram', 'Shita', 'Geeta'))
Output :
Array
(
    [1] => Ram
    [value] => Ram
    [0] => 0
    [key] => 0
)
Explanation: Here input array contain many elements
but ram is the current element so the output contains
its key and value pair. 

```

下面的程序演示了 PHP 中的 each()函数：

**程序 1**：

```php
<?php

$arr = array('maya', 'Sham', 'Geet');

print_r (each($arr));

?>
```

帖子主题：Re：Колибри

**程序 2**：

```php
<?php

$arr = array('a' => 'anny', 'b' => 'bunny', 
                           'c' => 'chinky');

reset($arr);

while (list($key, $val) = each($arr))
  {
      echo "$key => $val \n";
  }

?>
```

帖子主题：Re：Колибри

**参考**：[http://php.net/manual/en/function.each.php](http://php.net/manual/en/function.each.php)
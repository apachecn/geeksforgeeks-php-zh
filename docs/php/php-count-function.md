# PHP|count()函数

> Original: [https://www.geeksforgeeks.org/php-count-function/](https://www.geeksforgeeks.org/php-count-function/)

PHP 的这个内置函数用于计算数组中的当前元素。 对于已设置为空数组的变量，该函数可能返回 0。 另外，对于未设置的变量，函数返回 0。

**语法：**

```
count($array, mode)
```

**参数：**该函数一般只接受一个参数，即需要对其元素进行计数的数组。 但除此之外，函数可以接受参数*mode*，该参数告诉函数在正常模式或递归模式下对元素进行计数。

1.  **$array(必选)：**指需要统计其元素的数组。
2.  **模式(可选)：**用于设置功能的模式。 该参数可以接受两个可能的值，0 或 1.1。1 通常表示递归地计算数组的值。 这有助于对多维数组进行计数。 默认值为 0 或 False。

**返回值：**此函数返回数组中的元素数。

下面的程序将有助于理解 count()函数的工作原理。

**程序 1**：正常计数，即通过*模式*为 0 或不通过参数模式。

```
<?php

// PHP programme to illustrate working of count()
$array = array("Aakash", "Ravi", "Prashant", "49", "50");

print_r(count($array));

?>
```

产出：

```
5
```

**程序 2**：递归计数或将*模式*作为 1 传递。

```
<?php

// PHP program to illustrate working of count()
$array = array('names' => array('Aakash', 'Ravi', 'Prashant'),
               'rollno' => array('5', '10', '15'));

// recursive count - mode as 1
echo("Recursive count: ".count($array,1)."\n");

// normal count - mode as 0
echo("Normal count: ".count($array,0)."\n");

?>
```

产出：

```
Recursive count: 8
Normal count: 2

```

**参考**：
[http://php.net/manual/en/function.count.php](http://php.net/manual/en/function.count.php)
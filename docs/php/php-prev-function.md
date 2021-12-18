# PHP|prev()函数

> Original: [https://www.geeksforgeeks.org/php-prev-function/](https://www.geeksforgeeks.org/php-prev-function/)

Prev()函数是 PHP 中的内置函数。

*   它用于返回当前由内部指针指向的元素数组中的前一个元素。
*   我们已经讨论了 PHP 中的[CURRENT()](https://www.geeksforgeeks.org/php-current-function/)函数。
*   Current()函数用于返回当前由内部指针指向的元素的值，而 prev()函数用于递减或使内部指针指向当前指向的元素的前一个元素。

**语法：**

```
prev($array)
```

**参数：**此函数接受单个参数*$array*。 它是我们要查找其当前元素的数组。

**返回值**：它返回数组中位于内部指针当前指向的元素之前的元素的值。 如果数组为空，则 prev()函数返回 False。

以下程序说明了 PHP 中的 prev()函数：

**程序 1**：

```
<?php

// input array
$arr = array("Ram", "Shita", "Geeta", "Shyam");

// current function print the 
// 1st element of the array.
echo current($arr) ."\n";

// next function prints the next 
// element of the current one.
echo next($arr)."\n";

// prev function will print the previous element
// of the current one. As right now current element 
// is Shita so the previous element will be Ram
echo prev($arr);

?>
```

产出：

```
Ram
Shita
Ram

```

**程序 2**：

```
<?php

// input array
$arr = array('a', '2', 'z', '8');

// current function print the 
// 1st element of the array.
echo current($arr) ."\n";

// next function print the next 
// element of the current one.
echo next($arr)."\n";

// again next function print the 
// next element of the current one.
echo next($arr)."\n";

// prev function will print the previous element 
// of the current one. As right now current 
// element is 'z' so the previous element will be '2'
echo prev($arr);

?>
```

产出：

```
a
2
z
2

```

**引用：**
[http://php.net/manual/en/function.prev.php](http://php.net/manual/en/function.prev.php)
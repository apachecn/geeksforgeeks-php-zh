# PHP|Current()函数

> Original: [https://www.geeksforgeeks.org/php-current-function/](https://www.geeksforgeeks.org/php-current-function/)

Current()函数是 PHP 中的内置函数。

*   它用于返回内部指针当前指向的数组中元素的值。
*   CURRENT()函数**在返回值后不会递增或递减**内部指针。
*   在 PHP 中，所有数组都有一个内部指针。 此内部指针指向该数组中的某个元素，该元素称为数组的当前元素。
*   通常，当前元素是数组中第一个插入的元素。

**语法：**

```
current($rray)
```

**参数：**current()函数接受单个参数*$array*。 它是我们要查找其当前元素的数组。

**返回值：**它返回数组中内部指针当前指向的元素的值。 如果数组为空，则 current()函数返回 False。

**示例：**

```
Input : current(array("John", "b", "c", "d"))
Output : John
Explanation : Here as we see that input array contains 
many elements and the output is "John" because first 
element is John and current() function returns 
the element to which internal pointer is currently
pointing.

Input: current(array("abc", "123", "7"))
Output: abc
```

下面的程序演示了 PHP 中的 current()函数：

**程序 1**：

## PHP

```
<?php

// input array
$arr = array("Ram", "Shita", "Geeta");

// Here current function returns the
//  first element of the array.
echo current($a);

?>
```

**输出：**

```
Ram
```

**程序 2**：

## PHP

```
<?php

$arr = array('Sham', 'Mac', 'Jhon', 'Adwin');

// Here current element is Sham.
echo current($arr)."\n";

// increment internal pointer to point
// to next element i.e, Mac
echo next($arr)."\n";

// printing the current element as
// for now current element is Mac.
echo current($arr)."\n";

// increment internal pointer to point
// to next element i.e, Jhon.
echo next($arr)."\n";

// increment internal pointer to point
// to next element i.e, Adwin.
echo next($arr)."\n";

// printing the current element as for
// now current element is Adwin.
echo current($arr)."\n";

?>
```

**输出：**

```
Sham
Mac
Mac
Jhon
Adwin
Adwin
```

**注意：**当数组为空(即不包含任何元素)时，Current()函数返回 FALSE，当内部指针超出界限(即超出最后一个元素的末尾)时，函数也返回 FALSE。

**引用：**和
[http://php.net/manual/en/function.current.php](http://php.net/manual/en/function.current.php)
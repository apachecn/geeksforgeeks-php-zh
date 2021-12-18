# PHP|Reset()函数

> Original: [https://www.geeksforgeeks.org/php-reset-function/](https://www.geeksforgeeks.org/php-reset-function/)

函数的作用是：在 PHP 中内置函数。

*   此函数用于**将任何数组的内部指针移动到该数组的第一个元素。**
*   在处理数组时，我们可能会使用不同的函数修改数组的内部指针，如[prev()函数](https://www.geeksforgeeks.org/php-prev-function/)、[current()函数](https://www.geeksforgeeks.org/php-current-function/)、[key()函数](https://www.geeksforgeeks.org/php-key-function/)等。
*   函数的作用是：将内部指针重置为指向数组的第一个元素。

**语法：**

```php
reset($array)
```

**参数：**此函数接受单个参数*$array*。 它是我们想要重置其内部指针以再次指向第一个元素的数组。

**返回值**：成功时返回数组的第一个元素，如果数组为空，则返回 False，即不包含任何元素。

下面的程序演示了 PHP 中的 Reset()函数：

**程序 1：**

```php
<?php

// input array
$arr = array('Ram', 'Rahim', 'Geeta', 'Shita');

// here reset() function Moves the internal pointer to the
// first element of the array, which is Ram and also returns
// the first element
$res = reset($arr);
print "$res";

?>
```

产出：

```php
Ram
```

**程序 2：**

```php
<?php

// Input array
$arr = array('Delhi', 'Kolkata', 'London');

// getting current element using current()
// function
print current($arr)."\n";

// move internal pointer to next element
next($arr);

print current($arr)."\n";

// now reset() is called so that the internal pointer 
// moves to the first element again i.e, Delhi.
reset($arr);
print current($arr);

?>
```

产出：

```php
Delhi
Kolkata
Delhi

```

**引用：**
[http://php.net/manual/en/function.reset.php](http://php.net/manual/en/function.reset.php)
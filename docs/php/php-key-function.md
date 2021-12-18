# PHP|key()函数

> Original: [https://www.geeksforgeeks.org/php-key-function/](https://www.geeksforgeeks.org/php-key-function/)

Key()函数是 PHP 中的一个内置函数，用于返回内部指针当前指向的给定数组元素的索引。 当前元素可以是取决于光标位置的开始元素或下一个元素。 默认情况下，光标位置为零索引，即位于给定数组的起始元素。

**语法：**

```
key($array)
```

**参数：**此函数接受单个参数*$array*。 它是我们要为其查找由内部指针指向的当前元素的数组。

**返回值**：返回给定数组当前元素的索引。 如果输入数组为空，则 key()函数将返回 NULL。

以下程序说明了 PHP 中的 key()函数：

**程序 1**：

```
<?php

// input array 
$arr = array("Ram", "Geeta", "Shita", "Ramu");

// Here key function prints the index of 
// current element of the array.
echo "The index of the current element of".
                    " the array is: " . key($arr);

?>
```

产出：

```
The index of the current element of the array is: 0

```

**程序 2**：

```
<?php

// input array 
$arr=array("Ram", "Geeta", "Shita", "Ramu");

// next function increase the internal pointer
// to point next to the current element.
next($arr);

// Here key function prints the index of 
// the current element of the array.
echo "The index of the current element of".
                " the array is: " . key($arr);

?>
```

产出：

```
The index of the current element of the array is: 1

```

**程序 3**：

```
<?php

// input array 
$arr = array("0", "F", "D", "4");

// using next() function to increment
// internal pointer two times
next($arr);
next($arr);

// Here key function prints the index of
// element of the current array position.
echo "The index of the current element of".
                " the array is: " . key($arr);

?>
```

产出：

```
The index of the current element of the array is: 2

```

**引用：**
[http://php.net/manual/en/function.key.php](http://php.net/manual/en/function.key.php)
# PHP|range()函数

> Original: [https://www.geeksforgeeks.org/php-range-function/](https://www.geeksforgeeks.org/php-range-function/)

Range()函数是 PHP 中的一个内置函数，用于在给定范围(从低到高)内创建任何类型的元素数组，如整数、字母表，即列表的第一个元素被认为是低元素，最后一个元素被认为是高元素。

**语法：**

```php
*array* range(low, high, step)
```

**参数：**此函数接受三个参数，如下所述：

1.  **低：**它将是 range()函数生成的数组中的第一个值。
2.  **高：**它将是 range()函数生成的数组中的最后一个值。
3.  **步骤：**当范围内使用的增量且默认值为 1 时使用。

**返回值**：它从低到高返回一个元素数组。

例如：

```php
Input : range(0, 6)
Output : 0, 1, 2, 3, 4, 5, 6
Explanation: Here range() function print 0 to 
6 because the parameter of range function is 0 
as low and 6 as high. As the parameter step is 
not passed, values in the array are incremented 
by 1.

Input : range(0, 100, 10)
Output : 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100
Explanation: Here range() function accepts 
parameters as 0, 100, 10 which are values of low, 
high, step respectively so it returns an array with 
elements starting from 0 to 100 incremented by 10.

```

以下程序说明了 PHP 中的 range()函数：
**程序 1**：

```php
<?php

// creating array with elements from 0 to 6
// using range function
$arr = range(0,6);

// printing elements of array
foreach ($arr as $a) {

    echo "$a ";
}

?>
```

产出：

```php
0 1 2 3 4 5 6
```

**程序 2**：

```php
<?php

// creating array with elements from 0 to 100
// with difference of 20 between consecutive 
// elements using range function
$arr = range(0,100,20);

// printing elements of array
foreach ($arr as $a) {

    echo "$a ";
}

?>
```

产出：

```php
0 20 40 60 80 100
```

**程序 3**：

```php
<?php

// creating array with elements from a to j
// using range function
$arr = range('a','j');

// printing elements of array
foreach ($arr as $a) {

    echo "$a ";
}

?>
```

产出：

```php
a b c d e f g h i j
```

**程序 4**：

```php
<?php

// creating array with elements from p to a
// in reverse order using range function
$arr = range('p','a');

// printing elements of array
foreach ($arr as $a) {

    echo "$a ";
}

?>
```

产出：

```php
p o n m l k j i h g f e d c b a
```

**引用：**
[http://php.net/manual/en/function.range.php](http://php.net/manual/en/function.range.php)
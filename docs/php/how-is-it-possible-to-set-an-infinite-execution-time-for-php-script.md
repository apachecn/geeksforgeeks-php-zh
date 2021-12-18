# PHP 脚本怎么可能设置无限执行时间？

> 原文:[https://www . geesforgeks . org/如何设置 php 脚本的无限执行时间/](https://www.geeksforgeeks.org/how-is-it-possible-to-set-an-infinite-execution-time-for-php-script/)

是的，可以为 PHP 脚本设置无限的执行时间。我们可以通过在 PHP 脚本的开头添加 **set_time_limit()** 函数来实现。

**set_time_limit()** 函数只接受一个以秒为单位的 int 值参数，并返回一个布尔值。如果脚本达到给定的时间量，那么它会给出一个致命的错误。

**语法:**

```php
set_time_limit ( int $seconds )
```

**返回值:**布尔值(真或假)

**默认值:** 30 秒

对于最大值或者可以说无限执行时间，我们可以用 **0** 值设置函数。如果该值为 0，那么它将运行无限长的时间。

**注意:**只有在托管服务器允许你更改 PHP 配置的情况下，这个方法才会起作用。

**示例 1:** 以下示例是将执行时间设置为 40 秒

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

    // This will set the time limit to 40 seconds 
    // Default time is 30 seconds
    set_time_limit(40);
    $j=1;
    while($j<5)
    {
       echo "$j, ";
       $j++;
     }
?>
```

**输出:**

```php
 1, 2, 3, 4,
```

**示例 2:** 以下示例是最大(无限)时间的设置时间。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

    // This will set the time limit to infinite (maximum) 
    // Default time is 30 seconds
    set_time_limit(0);
    $j=1;
    while($j<50){
     echo "$j, ";
     $j++;
   }
?>
```

**输出:**

```php
1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 
17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 
32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46,
47, 48, 49,
```
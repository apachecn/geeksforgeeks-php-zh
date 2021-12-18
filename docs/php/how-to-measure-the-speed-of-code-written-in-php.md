# 如何衡量用 PHP 写代码的速度？

> 原文:[https://www . geesforgeks . org/如何测量用 php 编写代码的速度/](https://www.geeksforgeeks.org/how-to-measure-the-speed-of-code-written-in-php/)

使用时间戳功能来测量代码的速度。在程序中放置两次的时间戳函数，一次在程序开始时，另一次在程序结束时。那么结束时间和开始时间之间的时间差就是代码的实际速度。PHP 使用 [microtime($get_as_float)](https://www.geeksforgeeks.org/php-microtime-function/) 函数来衡量代码的速度。

**[micro time($ get _ as _ float)](https://www.geeksforgeeks.org/php-microtime-function/):**micro time()函数是 PHP 中的一个内置函数，用于以微秒为单位返回当前的 Unix 时间戳。$get_as_float 作为参数发送给 microtime()函数，默认情况下它返回字符串 microsec。

**语法:**

```php
microtime( $get_as_float )
```

**参数:**该函数接受单参数$get_as_float，可选。如果$get_as_float 设置为真，那么它指定函数应该返回一个浮点数，而不是字符串。

**返回类型:**默认返回字符串 microsec sec，其中 sec 为自 Unix Epoch(1970 年 1 月 1 日格林尼治时间 0:00:00)以来的秒数，microsc 为微秒部分。如果$get_as_float 参数设置为真，它将返回一个 float，表示自 Unix 纪元精确到最近的微秒以来的当前时间(以秒为单位)。

**示例 1:** 本示例使用 microtime()函数来测量代码的速度。

```php
<?php

// Use microtime() function to measure
// starting time
$time_start = microtime(true);

// Code of program
$num = 0;

for( $i = 0; $i < 100000000; $i += 1 ) {
    $num += 10;
}

// Use microtime() function to measure
// ending time
$time_end = microtime(true);

// Time difference
$time = $time_end - $time_start;

echo $time;

?>
```

**Output:**

```php
4.1413249969482

```

**例 2:** 该方法使用的是以秒为单位返回时间的 [time()](https://www.geeksforgeeks.org/php-time-function/) 函数，无法测出多少精确的执行时间。

```php
<?php

// Use time() function to measure
// starting time
$time_start = time();

// Code of program
$num = 0;
for( $i = 0; $i < 100000000; $i += 1) {
    $num += 10;
}

// Use time() function to measure
// ending time
$time_end = time();

// Time difference
$time = $time_end - $time_start;

echo $time;

?>
```

**Output:**

```php
4

```
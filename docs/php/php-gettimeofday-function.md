# PHP|gettimeofday()函数

> Original: [https://www.geeksforgeeks.org/php-gettimeofday-function/](https://www.geeksforgeeks.org/php-gettimeofday-function/)

Gettimeofday()函数是 PHP 中的内置函数，用于返回当前时间。 它是 Unix 系统调用 gettimeofday(2)的接口。 它返回一个包含从系统调用返回的数据的关联数组。 Float 选项作为参数发送给 gettimeofday()函数，并返回包含当前时间的关联数组。

**语法：**

```
gettimeofday( $return_float )
```

**参数：**此函数接受可选的单个参数*$Return_Float*。 此参数用于设置为 true，然后返回浮点值而不是数组。

**返回值：**返回包含当前时间的关联数组。 如果设置了*$RETURN_FLOAT*参数，则它返回浮点值。
关联数组由以下数组键组成：

*   **秒：**它用于指定从 Unix 纪元开始的秒数。
*   **usec：**它用于指定微秒。
*   **MinutesWest：**它用于指定格林威治以西的分钟数。
*   **dsttime：**用于指定 DST 校正的类型。

**异常：***$RETURN_FLOAT*参数是从 PHP 5.1.0 版本开始添加的。

下面的程序演示了 PHP 中的 gettimeofday()函数：

**程序 1：**

```
<?php

// Displaying the current time
// as an associative array
echo ("Current time is: ");
print_r(gettimeofday());
?>
```

**Output:**

```
Current time is: Array
(
    [sec] => 1536040360
    [usec] => 178383
    [minuteswest] => 0
    [dsttime] => 0
)

```

**程序 2：**

```
<?php

// Displaying the current time
// as a float value
echo ("Current time is: ");
print_r(gettimeofday(true));
?>
```

**Output:**

```
Current time is: 1536040361.1613

```

**相关文章：**

*   [PHP|gmstrftime()函数](https://www.geeksforgeeks.org/php-gmstrftime-function/)
*   [PHP|getdate()函数](https://www.geeksforgeeks.org/php-getdate-function/)
*   [PHP|gmmktime()函数](https://www.geeksforgeeks.org/php-gmmktime-function/)

**引用：**[http://php.net/manual/en/function.gettimeofday.php](http://php.net/manual/en/function.gettimeofday.php)
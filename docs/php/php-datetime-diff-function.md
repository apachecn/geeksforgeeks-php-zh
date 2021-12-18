# PHP|DateTime diff()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-diff-function/](https://www.geeksforgeeks.org/php-datetime-diff-function/)

**DateTime：：diff()函数**是 PHP 中的一个内置函数，用于返回两个给定 DateTime 对象之间的差值。

**语法：**

*   面向对象样式：

    ```
    *DateInterval* DateTime::diff( *DateTimeInterface* $datetime2,
                                      *bool* $absolute = FALSE )
    ```

    或

    ```
    *DateInterval* DateTimeImmutable::diff( *DateTimeInterface* $datetime2,
                                      *bool* $absolute = FALSE )
    ```

    或

    ```
    *DateInterval* DateTimeInterface::diff( *DateTimeInterface* $datetime2,
                                      *bool* $absolute = FALSE )
    ```

*   Process style:

    ```
    *DateInterval* date_diff( *DateTimeInterface* $datetime1,
                      *DateTimeInterface* $datetime2, *bool* $absolute = FALSE )
    ```

**参数：**此函数使用上述两个参数，如下所述：

*   **$datetime：**此参数保存要与第一个日期进行比较的日期。
*   **$Absolute：**此参数强制间隔为正。

**返回值：**此函数返回两个给定 DateTime 对象之间的差值。

下面的程序演示了 PHP 中的 datetime：：diff()函数：

**程序 1：**

```
<?php

// Initialising the two datetime objects
$datetime1 = new DateTime('2019-9-10');
$datetime2 = new DateTime('2019-9-15');

// Calling the diff() function on above
// two DateTime objects
$difference = $datetime1->diff($datetime2);

// Getting the difference between two
// given DateTime objects
echo $difference->format('%R%a days');
?>
```

**输出：**

```
+5 days

```

**程序 2：**

```
<?php

// Initialising the two datetime objects
$datetime1 = new DateTime('2019-8-10');
$datetime2 = new DateTime('2019-9-10');

// Calling the diff() function on above
// two DateTime objects
$difference = $datetime1->diff($datetime2);

// Getting the difference between two
// given DateTime objects
echo $difference->format('%R%a days');
?>
```

**输出：**

```
+31 days

```

**引用：**[https://www.php.net/manual/en/datetime.diff.php](https://www.php.net/manual/en/datetime.diff.php)
# PHP|gregoriantojd()函数

> Original: [https://www.geeksforgeeks.org/php-gregoriantojd-function/](https://www.geeksforgeeks.org/php-gregoriantojd-function/)

Gregoriantojd()函数是一个内置函数，用于将[公历日期](https://en.wikipedia.org/wiki/Gregorian_calendar)转换为[儒略日计数](https://en.wikipedia.org/wiki/Julian_calendar)。 该函数接受格式为*$Month/$day/$Year*的三个参数，表示公历中的日期，并将其转换为儒略日计数。

**语法：**

```
gregoriantojd( $month, $day, $year) 
```

**参数：**此函数接受三个必选参数，如上所示，如下所述：

1.  **$Month-**此参数指定公历中的月份编号。 月份数字在 1-12(含 1-12)范围内。 如果传递的月份数字大于 12 或小于 0，则儒略日返回为 0。
2.  **$day-**此参数指定公历中的日期。 天数在 1 到 31 之间(包括 1 和 31)。 如果传递的天数大于 31 或小于 0，则儒略日返回为 0。 闰年不在考虑之列。
3.  **$year –** This parameter specifies the year in Gregorian calendar.

    **返回值：**此函数返回转换为儒略日计数的公历日期。

    例如：

    ```
    Input : $month=3, $day=31, $year=2018 
    Output : 2458209

    Input : $month=4, $day=27, $year=2018
    Output : 2458236

    ```

    下面的程序演示了 gregoriantojd()函数。

    **程序 1：**下面的程序演示了 gregoriantojd()函数的用法。

    ```
    <?php
    // PHP program to demonstrate the
    // use of gregoriantojd() function 

    // converts date to julian integer 
    $jd=gregoriantojd(4, 27, 2018);

    // prints the julian day integer
    echo ($jd);
    ?>
    ```

    产出：

    ```
     2458236
    ```

    **程序 2：**下面的程序演示了日和月超出范围时的情况。

    ```
    <?php
    // PHP program to demonstrate the
    // use of gregoriantojd() function 

    // converts date to julian integer 
    // month is out of range
    $jd=gregoriantojd(4, 32, 2018);

    // prints the julian day integer
    echo ($jd), "\n"; 

    // day is out of range
    $jd=gregoriantojd(13, 29, 2018);
    echo ($jd); 
    ?>
    ```

    产出：

    ```
    0
    0
    ```

    **引用：**
    [http://php.net/manual/en/function.gregoriantojd.php](http://php.net/manual/en/function.gregoriantojd.php)
# PHP|jesishtojd()函数

> Original: [https://www.geeksforgeeks.org/php-jewishtojd-function/](https://www.geeksforgeeks.org/php-jewishtojd-function/)

函数的作用是：将[犹太日期](https://en.wikipedia.org/wiki/Hebrew_calendar)转换为[儒略日计数](https://en.wikipedia.org/wiki/Julian_calendar)。 该函数接受格式为*$Month/$day/$Year*的三个参数，表示犹太或希伯来语日历中的日期，并将其转换为儒略日计数。

**语法：**

```php
jewishtojd( $month, $day, $year) 
```

**参数：**此函数接受三个必选参数，如上所示，如下所述：

1.  **$Month-**此参数指定犹太日历中的月份编号。 月份数字在 1-13(含 1-13)的范围内。 如果传递的月份数字大于 12 或小于 1，则儒略日返回为 0。
2.  **$day-**此参数指定犹太日历中的日期。 天数在 1-30 之间(含 1-30 天)。 如果传递的天数大于 31 或小于 1，则儒略日返回为 0。 闰年不在考虑之列。
3.  **$year –** This parameter specifies the year in Jewish calendar. The year number is in range 1-9999 inclusive.

    **返回值：**此函数返回转换为儒略日计数的犹太日期。

    例如：

    ```php
    Input : $month=4, $day=8, $year=13
    Output : 352465

    Input : $month=4, $day=8, $year=898
    Output : 675707

    ```

    下面的程序说明了 jesishtojd()函数。

    **程序 1：**下面的程序演示了 jesishtojd()函数的用法。

    ```php
    <?php
    // PHP program to demonstrate the
    // use of jewishtojd() function 

    // converts date to julian integer 
    $jd = jewishtojd(4, 8, 13);

    // prints the julian day integer
    echo ($jd);
    ?>
    ```

    产出：

    ```php
    352465
    ```

    **程序 2：**下面的程序演示了日和月超出范围时的情况。

    ```php
    <?php
    // PHP program to demonstrate the
    // use of jewishtojd() function 

    // converts date to julian integer 
    // month is out of range
    $jd = jewishtojd(22, 8, 11);

    // prints the julian day integer
    echo ($jd), "\n"; 

    // day is out of range
    $jd=jewishtojd(4, 32, 11);
    echo ($jd); 
    ?>
    ```

    产出：

    ```php
    0
    0
    ```

    **引用：**
    [http://php.net/manual/en/function.jewishtojd.php](http://php.net/manual/en/function.jewishtojd.php)
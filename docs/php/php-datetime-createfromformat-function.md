# PHP|DateTime createFromFormat()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-createfromformat-function/](https://www.geeksforgeeks.org/php-datetime-createfromformat-function/)

**DateTime：：createFromFormat()函数**是 PHP 中的一个内置函数，它返回一个表示日期和时间格式的新 DateTime 对象。

**语法：**

*   Object-oriented style:

    ```
    *DateTime* DateTime::createFromFormat( *string* $format, 
                                        *string* $time, *DateTimeZone* $timezone )
    ```

*   Process style:

    ```
    *DateTime* date_create_from_format( *string* $format, 
                                        *string* $time, *DateTimeZone* $timezone )
    ```

**参数：**此函数使用三个参数，如上所述，如下所述：

*   **$format:** is a required parameter that specifies the date format. The following parameter strings are used in the format.
    1.  **date:**
        *   **d and j:** it describes the date of the month. It contains two numbers with or without leading zeros.
        *   The literal representation of **d and l:** for one day.
        *   **S:** the English serial number suffix of the month date, 2 characters. It is ignored in processing.
        *   **z:** date of the year (starting at 0)
    2.  **month:**
        *   **F and M:** the text representation of the month, such as January or September
        *   The number of **m and n:** months, with or without leading zeros
    3.  **year:**
        *   **Y:** full digital representation of the year, 4 digits
        *   **Y: two-digit representation of** year (assuming in the range 1970-2069, including)
    4.  **time:**
        *   **an and A: before and after** meridian
        *   **g and h:** 12-hour format with or without leading zeros
        *   **G and H:** 24-hour format with or without leading zeros
        *   **G and H:** 24-hour format. ]
        *   **I:** minutes, leading zero
        *   **s:** seconds with leading zero
        *   **u:** microseconds (up to 6 bits)
    5.  **time zone:**
        *   Time zone identifiers, or the hour difference with UTC, or the colon difference between hours and minutes and UTC, or the time zone abbreviation
    6.  **full date / time:**
        *   **U:** from the Unix era (00:00:00 GMT on January 1st, 1970)
    7.  **spaces and delimiters:**
        *   **(space): Tab**
        *   **#:** one of the following delimiters:;,:, /,., -, (Or)
        *   **;,:, /,., -, (Or): the character specified by** .
        *   **? :** random bytes
        *   ***:** random bytes up to the next delimiter or number
        *   **! :** resets all fields (year, month, day, hour, minute, second, score, and time zone information) to the Unix era
        *   **|:** reset all fields to the Unix era
        *   **|:** . Convert score and time zone information to Unix era (if they have not already been parsed)
        *   **+:** if this format specifier exists, the trailing data in the string will not cause an error, but will issue a warning
*   **$Time:** this parameter holds a string that represents the time.
*   **$TimeZone:** this parameter holds the DateTimeZone object that represents the desired time zone.

**返回值：**此函数成功时返回新的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 datetime：：createFromFormat()函数：

**程序 1：**

```
<?php

// Calling the DateTime:createFromFormat() function
// with the format 'j-M-Y' and given DateTime is 
$datetime = DateTime::createFromFormat('j-M-Y', '30-September-2019');

// Getting the new formatted datetime 
echo $datetime->format('Y-m-d');
?>
```

**输出：**

```
2019-09-30

```

**程序 2：**

```
<?php

// Calling the DateTime:createFromFormat() function
// with the format 'j-M-Y' and given DateTime is 
$datetime = DateTime::createFromFormat('j-M-Y', '1-oct-2019');

// Getting the new formatted datetime 
echo $datetime->format('d-m-Y H:i:s');
?>
```

**输出：**

```
01-10-2019 11:10:06

```

**引用：**[https://www.php.net/manual/en/datetime.createfromformat.php](https://www.php.net/manual/en/datetime.createfromformat.php)
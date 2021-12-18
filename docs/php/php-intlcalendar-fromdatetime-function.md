# PHP|IntlCalendar from mDateTime()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-fromdatetime-function/](https://www.geeksforgeeks.org/php-intlcalendar-fromdatetime-function/)

**IntlCalendar：：FromDateTime()函数**是 PHP 中的一个内置函数，用于从 DateTime 对象或字符串创建 IntlCalendar。 新日历的值表示与日期时间和时区相同的时刻。

**语法：**

*   Object-oriented style

    ```
    *IntlCalendar* IntlCalendar::fromDateTime( *mixed* $dateTime )
    ```

*   Process style

    ```
    *IntlCalendar* intlcal_from_date_time( *mixed* $dateTime )
    ```

**参数：**此函数接受单个参数**$dateTime**，该参数保存 DateTime 对象或可传递给 DateTime：：__Construct()函数的字符串。

**返回值：**此函数成功时返回 IntlCalendar 对象，失败时返回 NULL。 如果字符串作为参数传递，则 DateTime 构造函数内部会发生异常。

下面的程序演示了 PHP 中的 IntlCalendar：：FromDateTime()函数：

**程序 1：**

```
<?php 

// Create an IntlCalendar from a DateTime object or string 
$calendar = IntlCalendar::fromDateTime('2019-08-29 09:19:29'); 

// Add the date 
$calendar->add(IntlCalendar::FIELD_YEAR, 5); 

// Display the result date 
echo IntlDateFormatter::formatObject($calendar), "\n"; 

// Add the date 
$calendar->add(IntlCalendar::FIELD_YEAR, 10); 

// Display the result output 
echo IntlDateFormatter::formatObject($calendar), "\n"; 

// Add the date 
$calendar->add(IntlCalendar::FIELD_HOUR_OF_DAY, 10); 

// Display the result output 
echo IntlDateFormatter::formatObject($calendar); 

?> 
```

**输出：**

```
Aug 29, 2024, 9:19:29 AM
Aug 29, 2034, 9:19:29 AM
Aug 29, 2034, 7:19:29 PM

```

**程序 2：**

```
<?php 

// Create an IntlCalendar from a DateTime object or string 
$calendar = IntlCalendar::fromDateTime('2019-08-29 09:19:29'); 

// Add the date 
$calendar->add(IntlCalendar::FIELD_MONTH, 1); 

// Display the result date 
echo IntlDateFormatter::formatObject($calendar);

?> 
```

**输出：**

```
Sep 29, 2019, 9:19:29 AM

```

**引用：**[https://www.php.net/manual/en/intlcalendar.fromdatetime.php](https://www.php.net/manual/en/intlcalendar.fromdatetime.php)
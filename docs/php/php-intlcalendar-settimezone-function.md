# PHP|IntlCalendar setTimeZone()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-settimezone-function/](https://www.geeksforgeeks.org/php-intlcalendar-settimezone-function/)

**IntlCalendar：：setTimeZone()函数**是 PHP 中的一个内置函数，用于设置此日历的新时区。 时间是用对象表示的，它保留了不利于时区字段值的时间。

**语法：**

*   Object-oriented style

    ```
    *bool* IntlCalendar::setTimeZone( *mixed* $timeZone )
    ```

*   Process style

    ```
    *bool* intlcal_set_time_zone( *IntlCalendar* $cal, *mixed* $timeZone )
    ```

**参数：**此函数使用上述两个参数：

*   **$cal:** this parameter saves the resources of IntlCalendar.
*   **$TIMEZONE:** this parameter saves the new time zone used by this calendar.
    *   **null:** will use the default time zone.
    *   **IntlTimeZone:** is used directly.
    *   **DateTimeZone:** will extract the identifier of the DateTimeZone object and create an ICU time zone object.
    *   **string:** it should be a valid ICU time zone identifier.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 IntlCalendar：：setTimeZone()函数：

**程序：**

```
<?php

// Set the date timezone
ini_set('date.timezone', 'Asia/Calcutta');

// Create a DateTime object
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

// Format the DateTime object 
echo IntlDateFormatter::formatObject($calendar, IntlDateFormatter::FULL), "\n";

// Create new IntlGregorianCalendar object
$calendar->setTimezone(new DateTimeZone('Asia/Singapore')); 

// Format the DateTime object 
echo IntlDateFormatter::formatObject($calendar, IntlDateFormatter::FULL), "\n";

// Set the timezone
$calendar->setTimeZone('GMT+05:30');

// Format the DateTime object 
echo IntlDateFormatter::formatObject($calendar, IntlDateFormatter::FULL), "\n";

// Set the timezone
$calendar->setTimeZone(IntlTimeZone::getGMT());

// Format the DateTime object 
echo IntlDateFormatter::formatObject($calendar, IntlDateFormatter::FULL);

?>
```

**输出：**

```
Thursday, March 21, 2019 at 9:19:29 AM India Standard Time
Thursday, March 21, 2019 at 11:49:29 AM Singapore Standard Time
Thursday, March 21, 2019 at 9:19:29 AM GMT+05:30
Thursday, March 21, 2019 at 3:49:29 AM GMT

```

**引用：**[https://www.php.net/manual/en/intlcalendar.settimezone.php](https://www.php.net/manual/en/intlcalendar.settimezone.php)
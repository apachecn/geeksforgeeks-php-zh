# PHP|IntlCalendar setFirstDayOfWeek()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-setfirstdayofweek-function/](https://www.geeksforgeeks.org/php-intlcalendar-setfirstdayofweek-function/)

**IntlCalendar：：setFirstDayOfWeek()函数**是 PHP 中的一个内置函数，用于设置一周的开始日期。 此函数影响依赖于周的字段的行为，例如 IntlCalendar：：Field_Week_of_Year 和 IntlCalendar：：Field_Year_Woy。

**语法：**

*   Object-oriented style

    ```
    *bool* IntlCalendar::setFirstDayOfWeek( *int* $dayOfWeek )
    ```

*   Process style

    ```
    *bool* intlcal_set_first_day_of_week( *IntlCalendar* $cal, *int* $dayOfWeek )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$cal:** this parameter holds the resources of the IntlCalendar object.
*   **$DayOfWeek:** this parameter holds one of the field constants, such as IntlCalendar::DOW_SAUNDAY,IntlCalendar::DOW_MOUNDAY, …. , IntlCalendar::Dow_Satday .

**返回值：**如果成功，此函数返回 True，如果参数无效，则返回 False。

下面的程序演示了 PHP 中的 IntlCalendar：：setFirstDayOfWeek()函数：

**程序：**

```
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('intl.default_locale', 'es_ES');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Set the DateTime to the calendar object
$calendar->set(2019, 8, 25);

// Get first day of the week
var_dump($calendar->getFirstDayOfWeek());

// Set first day of the week
$calendar->setFirstDayOfWeek(IntlCalendar::DOW_SUNDAY);

// Get first day of the week
var_dump($calendar->getFirstDayOfWeek());

?>
```

**输出：**

```
int(2)
int(1)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.setfirstdayofweek.php](https://www.php.net/manual/en/intlcalendar.setfirstdayofweek.php)
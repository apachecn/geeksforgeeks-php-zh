# PHP|IntlCalendar get()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-get-function/](https://www.geeksforgeeks.org/php-intlcalendar-get-function/)

**IntlCalendar：：Get()函数**是 PHP 中的一个内置函数，用于获取特定字段的值。

**语法：**

*   Object-oriented style

    ```php
    *int* IntlCalendar::get( *int* $field )
    ```

*   Process style

    ```php
    *int* intlcal_get( *IntlCalendar* $cal, *int* $field )
    ```

**参数：**此函数使用上述两个参数：

*   **$cal:** this parameter saves the resources of IntlCalendar.
*   **$FIELD:** this parameter holds one of the IntlCalendar date / time field constants. This field contains an integer value between 0 and IntlCalendar::Field_Count.

**返回值：**此函数返回保存时间字段的值的整数。

下面的程序演示了 PHP 中的 IntlCalendar：：Get()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Declare the IntlCalendar class
$cls = new ReflectionClass('IntlCalendar');

// Declare an empty array
$arr = array();

// Loop for IntlCalendar constants
foreach ($cls->getConstants() as $constName => $constVal) {
    $arr[$constVal] = $constName;
}

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance();

// Display the date object
var_dump(IntlDateFormatter::formatObject($calendar));

// Loop to display result
foreach ($arr as $constVal => $constName) {
    echo "Constant Name: " . $constName . 
    "\nConstant Value: " . $calendar->get($constVal) . "\n\n";
}

?>
```

**输出：**

```php
string(25) "Sep 23, 2019, 11:03:29 AM"
Constant Name: WALLTIME_LAST
Constant Value: 1

Constant Name: WALLTIME_FIRST
Constant Value: 2019

Constant Name: WALLTIME_NEXT_VALID
Constant Value: 8

Constant Name: DOW_TYPE_WEEKEND_CEASE
Constant Value: 39

Constant Name: DOW_WEDNESDAY
Constant Value: 4

Constant Name: DOW_THURSDAY
Constant Value: 23

Constant Name: DOW_FRIDAY
Constant Value: 266

Constant Name: DOW_SATURDAY
Constant Value: 2

Constant Name: FIELD_DAY_OF_WEEK_IN_MONTH
Constant Value: 4

Constant Name: FIELD_AM_PM
Constant Value: 0

Constant Name: FIELD_HOUR
Constant Value: 11

Constant Name: FIELD_HOUR_OF_DAY
Constant Value: 11

Constant Name: FIELD_MINUTE
Constant Value: 3

Constant Name: FIELD_SECOND
Constant Value: 29

Constant Name: FIELD_MILLISECOND
Constant Value: 939

Constant Name: FIELD_ZONE_OFFSET
Constant Value: 19800000

Constant Name: FIELD_DST_OFFSET
Constant Value: 0

Constant Name: FIELD_YEAR_WOY
Constant Value: 2019

Constant Name: FIELD_DOW_LOCAL
Constant Value: 2

Constant Name: FIELD_EXTENDED_YEAR
Constant Value: 2019

Constant Name: FIELD_JULIAN_DAY
Constant Value: 2458750

Constant Name: FIELD_MILLISECONDS_IN_DAY
Constant Value: 39809939

Constant Name: FIELD_IS_LEAP_MONTH
Constant Value: 0

Constant Name: FIELD_FIELD_COUNT
Constant Value:

```

**引用：**[https://www.php.net/manual/en/intlcalendar.get.php](https://www.php.net/manual/en/intlcalendar.get.php)
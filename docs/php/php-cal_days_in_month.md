# PHP | cal_days_in_month()

> 原文:[https://www.geeksforgeeks.org/php-cal_days_in_month/](https://www.geeksforgeeks.org/php-cal_days_in_month/)

cal_days_in_month()是一个内置函数，它返回指定日历中特定月份的天数。我们必须传递日历类型、月份和年份作为参数，函数将返回日历中指定年份的月份中的天数。
**语法**

```php
int cal_days_in_month ( int $calendar, int $month, int $year )
```

**参数:**

*   **日历:**用于计算的日历类型。此值是必需的。
*   **月:**所选日历中的月。此值是必需的。
*   **年:**所选日历中的年。该值也是必需的。

下面是“日历”参数可以保存的可能值列表:

*   CAL_GREGORIAN
*   CAL_JULIAN
*   CAL _ JOSEPH
*   CAL _ FRENCH
*   CAL_NUM_CALS
*   卡尔·道·达诺
*   CAL_DOW_SHORT
*   CAL_DOW_LONG
*   CAL_MONTH_GREGORIAN_SHORT
*   CAL_MONTH_GREGORIAN_LONG
*   CAL_MONTH_JULIAN_SHORT
*   CAL_MONTH_JULIAN_LONG
*   CAL _ MONTH _ JUSION
*   CAL _ MONTH _ FRANCIS
*   CAL _ EASTER _ DEFAULT
*   CAL _ EASTER _ ROMAN
*   CAL _ EASTER _ ALWAYS _ GREGORIAN
*   CAL _ 复活节 _ 永远 _ 朱利安
*   CAL _ JOSEPH _ ADD _ ALAFIM _ GERESH
*   CAL _ JOSEPH _ ADD _ ALAFIM
*   CAL _ JOSEPH _ ADD _ GERESHAYIM

**返回值:**返回指定日历一年中某月的天数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<!DOCTYPE html>
<html>
<body>

<?php
$d = cal_days_in_month(CAL_GREGORIAN, 2, 1965); // Calendar Type - Gregorian
echo "There was $d days in February 1965.<br>";

$d = cal_days_in_month(CAL_GREGORIAN, 2, 2004); // Calendar Type - Gregorian
echo "There was $d days in February 2004.";
?>
</body>
</html>
```

**输出:**

```php
There was 28 days in February 1965.
There was 29 days in February 2004.
```
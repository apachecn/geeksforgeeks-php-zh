# PHP | cal_info()函数

> 原文:[https://www.geeksforgeeks.org/php-cal_info-function/](https://www.geeksforgeeks.org/php-cal_info-function/)

PHP 中的 cal_info()函数是一个内置函数，用于返回指定日历的信息。函数的作用是:返回一个包含 calname、month、缩写 month 和 maxdaysinmonth 以及 calsymbol 的数组。
以日历为参数，返回与指定日历相关的信息。

**语法:**

```
cal_info($calendar)
```

**参数:**PHP 中的 cal_info()函数只接受一个参数 *$calendar* 。此参数指定一个数字，表示您想要了解的日历。以下是可用作该参数值的有效数字列表。

*   0 = CAL_GREGORIAN
*   1 = CAL_JULIAN
*   2 = CAL _ JOSHY
*   3 = CAL _ FRENCH

**返回值:**返回指定日历的信息。

**错误和异常**:

1.  如果参数中没有指定日历，cal_info()函数将返回所有日历的信息。
2.  要将日历指定为 cal_info()函数的参数，需要提及其各自的数值，而不是日历名称，如公历的“0”。

下面的程序说明了 cal_info()函数。

**程序 1** :

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// displaying information
// regarding gregorian calendar
print_r (cal_info(0));

?>
```

输出:

```
Array
(
    [months] => Array
        (
            [1] => January
            [2] => February
            [3] => March
            [4] => April
            [5] => May
            [6] => June
            [7] => July
            [8] => August
            [9] => September
            [10] => October
            [11] => November
            [12] => December
        )

    [abbrevmonths] => Array
        (
            [1] => Jan
            [2] => Feb
            [3] => Mar
            [4] => Apr
            [5] => May
            [6] => Jun
            [7] => Jul
            [8] => Aug
            [9] => Sep
            [10] => Oct
            [11] => Nov
            [12] => Dec
        )

    [maxdaysinmonth] => 31
    [calname] => Gregorian
    [calsymbol] => CAL_GREGORIAN
)
```

**程序 2** :

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// displaying information
// regarding jewish calendar
print_r (cal_info(2));

?>
```

输出:

```
Array
(
    [months] => Array
        (
            [1] => Tishri
            [2] => Heshvan
            [3] => Kislev
            [4] => Tevet
            [5] => Shevat
            [6] => Adar I
            [7] => Adar II
            [8] => Nisan
            [9] => Iyyar
            [10] => Sivan
            [11] => Tammuz
            [12] => Av
            [13] => Elul
        )

    [abbrevmonths] => Array
        (
            [1] => Tishri
            [2] => Heshvan
            [3] => Kislev
            [4] => Tevet
            [5] => Shevat
            [6] => Adar I
            [7] => Adar II
            [8] => Nisan
            [9] => Iyyar
            [10] => Sivan
            [11] => Tammuz
            [12] => Av
            [13] => Elul
        )

    [maxdaysinmonth] => 30
    [calname] => Jewish
    [calsymbol] => CAL_JEWISH
)
```

**参考:**T2[http://php.net/manual/en/function.cal-info.php](http://php.net/manual/en/function.cal-info.php)T5】
# PHP|date_sunise()函数

> Original: [https://www.geeksforgeeks.org/php-date_sunrise-function/](https://www.geeksforgeeks.org/php-date_sunrise-function/)

Date_sunise()是 PHP 中的一个内置函数，用于查找指定日期和地点的日出时间。 此函数用于以指定格式返回成功时的日出时间。 失败时为 False。

**语法：**

```php
date_sunrise ( $timestamp, $format, $latitude, $longitude, $zenith, $gmtoffset )
```

**参数：**date_sunise()函数接受四个参数，如上所述，如下所述：

*   **$timeStamp:** this is a required parameter that specifies the timestamp of the date on which the sunrise time is obtained.
*   **$FORMAT:** optional parameter that specifies the format of the returned result.
    *   SfuUNCS_RET_STRING: returns a string. For example, 16:46 (default)
    *   SfuUNCS_RET_DOUBLE: returns a floating point number. For example, 16.78243132
    *   SfuUNCS_RET_TIMESTAMP: returns the result in the form of an integer (timestamp), such as 1095034606.
*   **$Latitude:** it is an optional parameter that specifies the latitude of the location. By default, it is set to North. To specify a value for South, pass in a negative value.
*   **$longitude:** this is an optional parameter that specifies the longitude of the location. By default, it is set to East. To modify the value of West, pass in a negative value.
*   **$zenith:** optional parameters. [the zenith](https://en.wikipedia.org/wiki/Zenith) is the angle between the center of the sun and the line perpendicular to the earth's surface. By default, it is date.sunrisezenith.
*   **$gmtoffset:** optional parameter that specifies the time difference in hours between Greenwich mean time and local time.

**返回值：**返回成功时指定格式的日出时间。 失败时为 False。

**异常：**如果日期/时间函数无效，此函数会生成 E_NOTICE 错误，如果使用系统设置或 TZ 环境变量，则会生成 E_STRICT 或 E_WARNING。

下面的程序演示了 date_sunise()函数。

**程序 1：**

```php
<?php
// PHP program to show sunrise time 
// of New delhi india for current day

// Longitude and latitude of Delhi India
// 28.6139° N, 77.2090° E
// GMT(Greenwich Mean Time) +5.30
// Zenith ~= 90

echo date("D M d Y");
echo("\nsunrise time: ");
echo(date_sunrise(time(), SUNFUNCS_RET_STRING,
                  28.6139, 77.2090, 90, 5.30));
?>
```

**输出：**

```php
Tue Jun 26 2018
sunrise time: 05:16

```

**程序 2：**

```php
<?php
// PHP program to show sunrise time 
// of GFG Noida for a Current day

// Longitude and latitude of GeeksforGeeks Noida
// 28°30'04.0"N 77°24'36.0"E
// GMT(Greenwich Mean Time) +5.30
// Zenith ~= 90

echo date("D M d Y");
echo("\nsunrise time: ");
echo(date_sunrise(time(), SUNFUNCS_RET_STRING,
              28.501120, 77.409989, 90, 5.30));
?>
```

**输出：**

```php
Tue Jun 26 2018
sunrise time: 05:15

```

**引用：**[http://php.net/manual/en/function.date-sunrise.php](http://php.net/manual/en/function.date-sunrise.php)
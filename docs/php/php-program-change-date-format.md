# 更改日期格式

的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-change-date-format/](https://www.geeksforgeeks.org/php-program-change-date-format/)

您将看到一个包含日期和时间的字符串。 日期为 dd/mm/yyyy 格式，时间为 12 小时格式。您必须转换为 yyyy/mm/dd 格式的日期和 24 小时格式的时间。

示例：

```
Input : $date = "12/05/2018 10:12 AM"
Output : 2018-05-12 10:12:00

Input : $date = "06/12/2014 04:13 PM"
Output : 2014-12-06 16:13:00

```

首先，我们将使用 strtotime()将日期转换为 Unix 时间戳，然后使用 date()将其转换为特定格式(strtotime()函数将英文文本日期时间解析为 Unix 时间戳(自 1970 年 1 月 1 日 00：00：00 GMT 以来的秒数))

```
<?php

    // function to convert string and print
    function convertString ($date)
    {
        // convert date and time to seconds
        $sec = strtotime($date);

        // convert seconds into a specific format
        $date = date("Y-m-d H:i", $sec);

        // append seconds to the date and time
        $date = $date . ":00";

        // print final date and time
        echo $date;
    }

    // Driver code
    $date = "06/12/2014 04:13 PM";
    convertString($date);
?>
```

**输出：**

```
2014-06-12 16:13:00

```
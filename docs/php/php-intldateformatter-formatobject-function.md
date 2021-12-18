# PHP|IntlDateForMatter Format Object()函数

> Original: [https://www.geeksforgeeks.org/php-intldateformatter-formatobject-function/](https://www.geeksforgeeks.org/php-intldateformatter-formatobject-function/)

**IntlDateForMatter：：FormatObject()函数**是 PHP 中的一个内置函数，用于格式化 IntlDateForMatter 对象。 此函数允许格式化 IntlCalendar 或 DateTime 对象。

**语法：**

*   Object-oriented style:

    ```php
    *string* IntlDateFormatter::formatObject( *object* $object, 
                             *mixed* $format = NULL, *string* $locale = NULL )
    ```

*   Process style:

    ```php
    *string* datefmt_format_object( *object* $object,
                             *mixed* $format = NULL, *string* $locale = NULL )
    ```

**参数：**此函数接受上述三个参数，如下所述：

*   **object:** this parameter saves objects of type IntlCalendar or DateTime.
*   **format:** this parameter saves the format of the date and is used to set the date of the given format. You can use an array with two values (the first to set the date style and the second to set the time style). Constants are in IntlDateForMatter::None, IntlDateForMatter::Short, IntlDateForMatter::Medium, IntlDateForMatter::Long, IntlDateForMatter::Full), integer, or string format. Null values are used for the default style.
*   **locale:** this parameter saves the locale used. Null values are used for the default locale.

**返回值：**此函数成功时返回给定格式的字符串，失败时返回 False。

下面的程序演示了 PHP 中的 IntlDateForMatter：：FormatObject()函数：

**程序：**

```php
<?php

// Set the timezone and locale
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('intl.default_locale', 'en_US');

// Create an IntlCalendar from a DateTime object or string 
$calander = IntlCalendar::fromDateTime('2019-10-05 09:19:29');  

// Display the date in given format
echo "Default date format => " .
    IntlDateFormatter::formatObject($calander) . "\n";

// Display the date in given format
echo "Date in string format => " .
    IntlDateFormatter::formatObject($calander,
    "dd MM yyyy") . "\n";

// Display the date in given format
echo "Date in long format => " .
    IntlDateFormatter::formatObject($calander,
    IntlDateFormatter::TRADITIONAL) . "\n";

// Display the date in given format
echo "Date in array format => ",
    IntlDateFormatter::formatObject($calander, 
    array(
        IntlDateFormatter::NONE,
        IntlDateFormatter::FULL)
    );

?>
```

**输出：**

```php
Default date format => Oct 5, 2019, 9:19:29 AM
Date in string format => 05 10 2019
Date in long format => Saturday, October 5, 2019 at 9:19:29 AM India Standard Time
Date in array format => 9:19:29 AM India Standard Time

```

**引用：**[https://www.php.net/manual/en/intldateformatter.formatobject.php](https://www.php.net/manual/en/intldateformatter.formatobject.php)
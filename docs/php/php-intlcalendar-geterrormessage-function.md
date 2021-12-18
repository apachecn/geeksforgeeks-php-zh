# PHP|IntlCalendar getErrorMessage()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-geterrormessage-function/](https://www.geeksforgeeks.org/php-intlcalendar-geterrormessage-function/)

**IntlCalendar：：getErrorMessage()函数**是 PHP 中的一个内置函数，用于使用 IntlCalendar：：getErrorCode()或 intlcal_get_error_code()函数返回与错误相关的错误消息(如果存在任何错误)。

**语法：**

*   Object-oriented style

    ```
    *string* IntlCalendar::getErrorMessage( *void* )
    ```

*   Process style

    ```
    *string* intlcal_get_error_message( *IntlCalendar* $calendar )
    ```

**参数：**此函数使用单个参数**$caleal**，该参数保存过程化样式界面上的日历对象。

**返回值：**此函数返回与此对象的函数调用中发生的最后一个错误相关的错误消息，或返回指示不存在错误的字符串。

下面的程序演示了 PHP 中的 IntlCalendar：：getErrorMessage()函数：

**程序：**

```
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Set the intl error level
ini_set("intl.error_level", E_WARNING);

// Declare a DateTime object and store it into variable
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

// Display the error code and message
var_dump($calendar->getErrorMessage());

// Declare a DateTime object and store it into variable
$calendar->fieldDifference(-34E403, IntlCalendar::FIELD_ZONE_OFFSET);

// Display the error code and message
var_dump($calendar->getErrorMessage());

?>
```

**输出：**

```
PHP Warning:  IntlCalendar::fieldDifference(): intlcal_field_difference: Call to ICU method has
failed in /home/22bd84b151f5397224d747dadc65338e.php on line 16
string(12) "U_ZERO_ERROR"
string(81) "intlcal_field_difference: Call to ICU method has failed: U_ILLEGAL_ARGUMENT_ERROR"

```

**引用：**[https://www.php.net/manual/en/intlcalendar.geterrormessage.php](https://www.php.net/manual/en/intlcalendar.geterrormessage.php)
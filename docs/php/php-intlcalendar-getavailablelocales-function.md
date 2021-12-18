# PHP|IntlCalendar getAvailableLocales()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-getavailablelocales-function/](https://www.geeksforgeeks.org/php-intlcalendar-getavailablelocales-function/)

**IntlCalendar：：getAvailableLocales()函数**是 PHP 中的一个内置函数，用于显示安装日历的区域设置的数组列表。

**语法：**

*   Object-oriented style

    ```php
    *array* IntlCalendar::getAvailableLocales( *void* )
    ```

*   Process style

    ```php
    *array* intlcal_get_available_locales( *void* )
    ```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含区域设置值的字符串数组。

下面的程序演示了 PHP 中的 IntlCalendar：：getAvailableLocales()函数：

**程序 1：**

```php
<?php

// Use IntlCalendar::getAvailableLocales() function
// to get the locale list
var_dump(IntlCalendar::getAvailableLocales());

?>
```

**输出：**

```php
array(683) {
  [0]=>
  string(2) "af"
  [1]=>
  string(5) "af_NA"
  [2]=>
  string(5) "af_ZA"
  [3]=>
  string(3) "agq"
  [4]=>
  string(6) "agq_CM"
  [5]=>
  string(2) "ak"
  ...
}

```

**程序 2：**

```php
<?php

// Use intlcal_get_available_locales() function
// to get the list of locale
var_dump(intlcal_get_available_locales());

?>
```

**输出：**

```php
array(683) {
  [0]=>
  string(2) "af"
  [1]=>
  string(5) "af_NA"
  [2]=>
  string(5) "af_ZA"
  [3]=>
  string(3) "agq"
  [4]=>
  string(6) "agq_CM"
  [5]=>
  string(2) "ak"
  ...
}

```

**引用：**[https://www.php.net/manual/en/intlcalendar.getavailablelocales.php](https://www.php.net/manual/en/intlcalendar.getavailablelocales.php)
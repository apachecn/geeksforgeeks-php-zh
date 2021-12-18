# PHP|DateTime Format()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-format-function/](https://www.geeksforgeeks.org/php-datetime-format-function/)

**DateTime：：Format()函数**是 PHP 中的一个内置函数，用于根据指定的格式返回新的格式化日期。

**语法：**

*   面向对象样式

    ```
    *string* DateTime::format( *string* $format )
    ```

    或

    ```
    *string* DateTimeImmutable::format( *string* $format )
    ```

    或

    ```
    *string* DateTimeInterface::format( *string* $format )
    ```

*   Process style

    ```
    *string* date_format( *DateTimeInterface* $object, *string* $format )
    ```

**参数：**此函数使用上述两个参数，如下所述：

*   **$Object：**此参数保存 DateTime 对象。
*   **$Format：**此参数保存 date()函数接受的格式。

**返回值：**此函数成功时返回新格式化的日期字符串，失败时返回 False。

下面的程序演示了 PHP 中的 DateTime：：Format()函数：

**程序 1：**

```
<?php

// Initialising the DateTime() object with a date
$datetime = new DateTime('2019-09-30');

// Calling the format() function with a 
// specified format 'd-m-Y'
echo $datetime->format('d-m-Y');

?>
```

**输出：**

```
30-09-2019

```

**程序 2：**

```
<?php

// Initialising the DateTime() object with a date
$datetime = new DateTime('2019-09-30');

// Calling the format() function with a 
// specified format 'd-m-Y H:i:s'
echo $datetime->format('d-m-Y H:i:s');

?>
```

**输出：**

```
30-09-2019 00:00:00

```

**引用：**[https://www.php.net/manual/en/datetime.format.php](https://www.php.net/manual/en/datetime.format.php)
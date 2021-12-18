# PHP|DateTime add()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-add-function/](https://www.geeksforgeeks.org/php-datetime-add-function/)

**DateTime：：add()函数**是 PHP 中的一个内置函数，用于向给定的 DateTime 对象添加一段时间(天、月、年、小时、分钟和秒)。

**语法：**

*   Object-oriented style:

    ```
    *DateTime* DateTime::add( *DateInterval* $interval )
    ```

*   Process style:

    ```
    *DateTime* date_add( *DateTime* $object, *DateInterval* $interval )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$object:** it specifies the DateTime object returned by the date_create () function. This function returns a new DateTime object.
*   **$Interval:** this parameter saves the DateInterval object.

**返回值：**此函数成功更改后返回新的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DateTime：：Add()函数：

**程序 1：**

```
<?php

// Initialising a DateTime
$datetime = new DateTime('2019-09-30');

// DateInterval object is taken as the 
// parameter of the add() function
// Here 1 day is added
$datetime->add(new DateInterval('P1D'));

// Getting the new date after addition
echo $datetime->format('Y-m-d') . "\n";
?>
```

**输出：**

```
2019-10-01

```

**程序 2：**

```
<?php

// Initialising a DateTime
$datetime = new DateTime('2019-09-30');

// DateInterval object is taken as the 
// parameter of the add() function
// Here 5 hours, 3 Minutes and 10 seconds is added
$datetime->add(new DateInterval('PT5H3M10S'));

// Getting the new date after addition
echo $datetime->format('Y-m-d H:i:s') . "\n";
?>
```

**输出：**

```
2019-09-30 05:03:10

```

**引用：**[https://www.php.net/manual/en/datetime.add.php](https://www.php.net/manual/en/datetime.add.php)
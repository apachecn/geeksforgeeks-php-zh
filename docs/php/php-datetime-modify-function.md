# PHP|DateTime Modify()函数

> Original: [https://www.geeksforgeeks.org/php-datetime-modify-function/](https://www.geeksforgeeks.org/php-datetime-modify-function/)

**DateTime：：Modify()函数**是 PHP 中的一个内置函数，用于修改或可以更改 DateTime 对象的时间戳。

**语法：**

*   Object-oriented style:

    ```php
    *DateTime* DateTime::modify( *string* $modify )
    ```

*   Process style:

    ```php
    *DateTime* date_modify( *DateTime* $object, *string* $modify )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$object:** it specifies the DateTime object returned by the date_create () function. This object is modified by the DateTime::Modify () function.
*   **$Modify:** it specifies the date / time string. It is incremented or decremented to modify the DateTime object.

**返回值：**此函数成功时返回修改后的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 DateTime：：Modify()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate 
// DateTime::modify() function

// Creating a DateTime object
$datetime = new DateTime('2019-09-30');

// Calling of date DateTime::modify() function
// with the increment of 5 days as parameters
$datetime->modify('+5 day');

// Getting the modified date in "y-m-d" format
echo $datetime->format('Y-m-d');

?>
```

**输出：**

```php
2019-10-05

```

**程序 2：**

```php
<?php
// PHP program to illustrate the
// DateTime::modify() function

// Creating a DateTime object
$datetime = new DateTime('2019-09-30');

// Calling of date DateTime::modify() function
// with the increment of 5 months as parameters
$datetime->modify('+5 month');

// Getting the modified date in "y-m-d" format
echo $datetime->format('Y-m-d');

?>
```

**输出：**

```php
2020-03-01

```

**引用：**[https://www.php.net/manual/en/datetime.modify.php](https://www.php.net/manual/en/datetime.modify.php)
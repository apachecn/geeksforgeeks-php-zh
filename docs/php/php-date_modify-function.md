# PHP|Date_Modify()函数

> Original: [https://www.geeksforgeeks.org/php-date_modify-function/](https://www.geeksforgeeks.org/php-date_modify-function/)

DATE_MODIFY()函数是 PHP 中的内置函数。 通过此函数，我们可以修改或更改 DateTime 对象的时间戳。 DateTime 对象和 String Modify 是调用函数中的参数。

**语法：**

```php
date_modify(DateTime $object, string $modify);

```

**参数：**
该函数接受两个参数，如下所述：

1.  **$Object**：这是必选参数。 它指定由[DATE_CREATE()](https://www.geeksforgeeks.org/php-date_create-date_format-add_date-functions/)返回的 DateTime 对象。该对象由上面提到的函数修改。
2.  **$Modify**：这也是必选参数。 它指定日期/时间字符串。 它是递增或递减的，以修改 DateTime 对象。

**返回值**：
此函数在成功时返回 DateTime*对象*。 并在失败时返回 FALSE。

以下程序说明了 date_Modify()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate date_modify()
// function

// creating DateTime object
$date=date_create("2018-04-08");

// calling of date modify function
// with two required parameters 
date_modify($date, "+15 days"); 

// printing the modified date in "y-m-d" format
echo date_format($date, "Y-m-d");
?>
```

发帖主题：Re：Колибри0.7.0

```php
2018-04-13

```

**计划 2**：此计划将增加一个月

```php
<?php
// PHP program to illustrate date_modify()
// function

// creating a DateTime object
$date = date_create('2000-10-14');

// calling date_modify function with 
// two required parameters
date_modify($date, '+1 month');

// printing the modified date
echo date_format($date, 'Y-m-d');
?>
```

发帖主题：Re：Колибри0.7.0

```php
2000-11-14

```

**参考**
[http://php.net/manual/en/datetime.modify.php](http://php.net/manual/en/datetime.modify.php)
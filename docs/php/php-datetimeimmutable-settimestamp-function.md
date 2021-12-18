# PHP|DateTimeImmutable setTimestamp()函数

> Original: [https://www.geeksforgeeks.org/php-datetimeimmutable-settimestamp-function/](https://www.geeksforgeeks.org/php-datetimeimmutable-settimestamp-function/)

**DateTimeImmutable：：setTimestamp()函数**是 PHP 中的一个内置函数，用于根据 Unix 时间戳设置日期和时间。

**语法：**

```
*DateTimeImmutable* DateTimeImmutable::setTimestamp( *int* $unixtimestamp )

```

**参数：**此函数接受单个参数**$unixtimeStamp**，该参数用于设置表示日期的 Unix 时间戳。

**返回值：**此函数返回 DateTimeImmutable 对象。

下面的程序演示了 PHP 中的 DateTimeImmutable：：setTimestamp()函数：

**程序 1：**

```
<?php
// PHP program to illustrate DateTimeImmutable::setTimestamp()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Initialising a unixtimestamp
$unixtimestamp = '1171564674';

// Calling the DateTimeImmutable::setTimestamp() function
$a = $datetimeImmutable->setTimestamp($unixtimestamp);

// Getting a new set of date and time in the
// format of 'U = d-m-Y H:i:s'
echo $datetimeImmutable->format('U = d-m-Y H:i:s');
?>
```

**输出：**

```
1570187170 = 04-10-2019 11:06:10

```

**程序 2：**

```
<?php
// PHP program to illustrate DateTimeImmutable::setTimestamp()
// function

// Creating a new DateTimeImmutable() object
$datetimeImmutable = new DateTimeImmutable();

// Calling the DateTimeImmutable::setTimestamp() function
// with the parameter of unixtimestamp
$a = $datetimeImmutable->setTimestamp(1291564453);

// Getting a new set of date and time in the
// format of 'U = d-m-Y H:i:s'
echo $datetimeImmutable->format('U = d-m-Y H:i:s');
?>
```

**输出：**

```
1570187171 = 04-10-2019 11:06:11

```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.settimestamp.php](https://www.php.net/manual/en/datetimeimmutable.settimestamp.php)
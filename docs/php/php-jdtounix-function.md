# PHP|jdtounix()函数

> Original: [https://www.geeksforgeeks.org/php-jdtounix-function/](https://www.geeksforgeeks.org/php-jdtounix-function/)

PHP 中的 jdtounix()函数是一个内置函数，用于将儒略日日期转换为 Unix 时间戳。 此函数返回与儒略日对应的 Unix 时间戳，该时间戳用作参数；如果输入的日期不在 Unix 纪元内，即 1970 年和 2037 年之间的公历年份或 2440588<=儒略日日期<=2465342，则返回 FALSE。

函数的作用是：根据世界协调时间(UTC)返回时间。

**语法：**

```php
jdtounix($jd)
```

**参数：**PHP 中的 jdtounix()函数只接受一个参数*$jd*。 此参数指定介于 2440588 和 2465342 之间的儒略日数字。

**返回值：**它返回与儒略日对应的 Unix 时间戳作为参数，如果输入的日期不在 Unix 纪元内，则返回 False。

**错误和异常**：

1.  用作参数的儒略日期必须在 2440588-2465342 范围内。
2.  Jdtounix()函数忽略儒略日计数的小数部分，因此在许多情况下可能会给出不正确的结果。

**示例：**

```php
Input : $julian_date = gregoriantojd(01, 02, 1997);
        echo jdtounix($julian_date);
Output : 852163200

Input : $julian_date = gregoriantojd(11, 21, 2017);
        echo jdtounix($julian_date);
Output : 1511222400

```

以下程序说明了 jdtounix()函数：

**程序 1**：

```php
<?php

// converting Gregorian date to Julian date
$julian_date = gregoriantojd(01, 02, 1997);

// Converting Julian date to Unix Timestamp
echo jdtounix($julian_date);

?>
```

产出：

```php
852163200
```

**程序 2**：

```php
<?php

// converting Gregorian date to Julian date
$julian_date=gregoriantojd(11, 21, 2017);

// Converting Julian date to Unix Timestamp
echo jdtounix($julian_date);

?>
```

产出：

```php
1511222400
```

**引用：**
[http://php.net/manual/en/function.jdtounix.php](http://php.net/manual/en/function.jdtounix.php)
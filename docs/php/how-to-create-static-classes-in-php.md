# 如何用 PHP 创建静态类？

> 原文:[https://www . geesforgeks . org/how-create-static-class-in-PHP/](https://www.geeksforgeeks.org/how-to-create-static-classes-in-php/)

类是用户定义的数据类型，它保存自己的数据成员和成员函数，可以通过创建该类的一个或多个实例来访问和使用。每次实例化一个类时，它所保存的值对于特定的实例或对象是不同的和唯一的，而对于该类则不是。**静态类**带来了一个属性，其中类本身保存的值保持不变并且不是唯一的。静态类的另一个特性是，我们可以在不创建类实例的情况下完成上述工作。

**如何创建静态类？**
相当简单。在类中声明和定义的变量和方法将使用 [static 关键字](https://www.geeksforgeeks.org/static-function-in-php/)声明为静态的，这样它们就可以在不首先实例化类的情况下使用。
这里需要注意的一点是，既然这意味着一个类变量可以在没有特定实例的情况下被访问，那么这也意味着这个变量将只有一个版本。另一个后果是静态方法不能访问非静态变量和方法，因为它们需要类的实例。

要访问静态类及其方法，请使用以下语法:

```php
 ClassName::MethodName();
```

**示例 1:** 以下代码返回当前日期，而不实例化类 date。在这种情况下，日期的**格式与实际日期不变。**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class Date {

    public static $date_format1 = 'F jS, Y';
    public static $date_format2 = 'Y/m/d H:i:s';
    public static function format_date($unix_timestamp) {
        echo date(self::$date_format1, $unix_timestamp), "\n";
        echo date(self::$date_format2, $unix_timestamp);
    }
}

echo Date::format_date(time());
?>
```

```php
Output:
April 30th, 2020
2020/04/30 10:48:36
```

**示例 2:** 以下代码检查字符串是否有效。如果长度等于 13，则有效。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class geeks {

    public static $x = 13;

    public static function isValid($s) {
        if(strlen($s) == self::$x )
            return true;
        else
            return false;
    }
}

$s1 = "geeksforgeeks";
if(geeks::isValid($s1))
    echo "String is valid! \n";
else
    echo "String is NOT valid! \n";

$s2 = "geekforgeek";

if(geeks::isValid($s2))
    echo "String is valid!\n ";
else
    echo "String is NOT valid! \n";
?>
```

**输出:**

```php
String is valid!
String is NOT valid!
```
# 如何在 PHP 中复制一个 DateTime 对象？

> 原文:[https://www . geesforgeks . org/how-to-copy-a-datetime-object-in-PHP/](https://www.geeksforgeeks.org/how-to-copy-a-datetime-object-in-php/)

给定一个日期时间对象，任务是创建该对象的副本。要创建日期时间对象的副本，我们使用克隆关键字，如下所述:
日期时间对象的副本是通过使用克隆关键字(如果可能，该关键字调用对象的 __clone()方法)创建的。不能直接调用对象的 __clone()方法。当一个对象被克隆时，PHP 将对该对象的所有属性执行一个浅拷贝。任何引用其他变量的属性都将保持引用状态。

**语法:**

```
$DateTime_copy_object_name = clone $DateTime_object_to_be_copied
```

下面的例子说明了在 PHP 中日期时间对象的克隆:

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to create copy of DateTime object

// Creating object
$obj = new DateTime();

// Creating clone or copy of object
$copy = clone $obj;

// Printing initial values
echo "Printing initial values\n";

$result = $obj->format('Y-m-d H:i:s');
echo "Original object: $result\n";

$result = $copy->format('Y-m-d H:i:s');
echo "Cloned object: $result\n\n";

// Changing original object ($obj) value
// to verify other($copy) is clone or not

// This statement will add 3 Days
$obj->add(new DateInterval('P3D'));

// Printing values
echo "Printing values after change\n";

$result = $obj->format('Y-m-d H:i:s');
echo "Original object: $result\n";

$result = $copy->format('Y-m-d H:i:s');
echo "Cloned object: $result\n";
?>
```

**输出:**

```
Printing initial values
Original object: 2020-04-14 17:14:18
Cloned object: 2020-04-14 17:14:18

Printing values after change
Original object: 2020-04-17 17:14:18
Cloned object: 2020-04-14 17:14:18
```

**示例 2:** 下面的程序将克隆与赋值(=)运算符区分开来。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to create copy of DateTime object

// Creating object
$obj = new DateTime();

// Creating clone or copy of object
$copy = clone $obj;

$ref_obj = $obj;

// Printing initial values
echo "Printing initial values\n";

$result = $obj->format('Y-m-d H:i:s');
echo "Original object: $result\n";

$result = $ref_obj->format('Y-m-d H:i:s');
echo "Reference object: $result\n";

$result = $copy->format('Y-m-d H:i:s');
echo "Cloned object: $result\n\n";

// Changing original object ($obj) value
// to verify other($copy) is clone or not

// This statement will add 3 Months
$obj->add(new DateInterval('P3M'));

// Printing values
echo "Printing values after change\n";

$result = $obj->format('Y-m-d H:i:s');
echo "Original object: $result\n";

$result = $ref_obj->format('Y-m-d H:i:s');
echo "Reference object: $result\n";

$result = $copy->format('Y-m-d H:i:s');
echo "Cloned object: $result\n";
?>
```

**输出:**

```
Printing initial values
Original object: 2020-04-14 17:14:49
Reference object: 2020-04-14 17:14:49
Cloned object: 2020-04-14 17:14:49

Printing values after change
Original object: 2020-07-14 17:14:49
Reference object: 2020-07-14 17:14:49
Cloned object: 2020-04-14 17:14:49
```

因此，要复制我们使用 clone 的对象，不要使用(=)运算符，因为它会创建一个引用。
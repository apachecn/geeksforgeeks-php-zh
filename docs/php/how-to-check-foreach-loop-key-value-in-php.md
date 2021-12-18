# PHP 中如何检查 foreach 循环键值？

> 原文:[https://www . geesforgeks . org/how-check-foreach-loop-key-value-in-PHP/](https://www.geeksforgeeks.org/how-to-check-foreach-loop-key-value-in-php/)

在 PHP 中，[**foreach**](https://www.geeksforgeeks.org/php-foreach-loop/) 循环可用于循环元素数组。它可以通过多种方式使用，例如

1.  Loop through a series of simple values.
2.  Traverse the list of key-value pairs.

**使用带有简单值的 foreach 循环:**

我们可以使用 *foreach* 循环来访问和使用简单值数组中的元素，例如字符串或数字。

**例 1:**

## PHP

```
<?php
    $names = array("Ramesh", "Suresh", "Ram", "Shyam");
    foreach ($names as $value) {
    echo "$value <br>";
    }
?>
```

**输出:**

```
Ramesh
Suresh
Ram
Shyam
```

在上面的例子中，名为的数组**的每个元素被迭代并被分配给变量**值。****

**例 2:**

## PHP

```
<?php
    $marks = array(45, 78, 93, 69);
    foreach ($marks as $value) {
      echo "$value <br>";
    }
?>
```

**输出:**

```
45
78
93
69
```

**使用带有键值对的 foreach 循环:**

我们将使用相同的 foreach 循环来迭代键值对数组。

**例 3:** 在这种情况下，一个学生的数组和他们的分数都在数组中。

## PHP

```
<?php
    $markSheet = array("Ramesh"=>45, "Suresh"=>78, "Ram"=>93, "Shyam"=>69);
    foreach ($markSheet as $key => $val) {
      echo "$key - $val<br>";
    }
?>
```

**输出:**

```
Ramesh - 45
Suresh - 78
Ram - 93
Shyam - 69
```

在上例中，我们迭代每个数组元素，然后将键值对分别提取为变量 **key** 和 **val** 。
# 如何在 PHP 中启动和停止定时器？

> 原文:[https://www . geesforgeks . org/如何启动和停止 php 中的计时器/](https://www.geeksforgeeks.org/how-to-start-and-stop-a-timer-in-php/)

您可以使用 PHP 中的 [**【微时间()**](https://www.geeksforgeeks.org/php-microtime-function/) 功能来启动和停止 PHP 中的计时器。 **microtime()** 函数是 PHP 中的一个内置函数，用于以微秒为单位返回当前的 Unix 时间戳。

在本文中，您将学习 **microtime()** 函数的用法。

**语法:**

```php
microtime( $get_as_float )
```

*   **Parameter:** *$ get _ as _ float* is sent to the **microtime ()** function as a parameter, and the string microsec is returned by default.
*   **Return value:** By default, **microtime ()** function returns time as a string, but if set to TRUE, it returns time as a string. So the default value is FALSE.

**示例 1:** 以下示例使用 *false* 作为**微时间()**方法的参数。

## PHP

```php
<?php

  // Displaying the micro time as a string
  echo ("Displaying the micro time as a string :");
  echo(microtime());
?>
```

**输出**

```php
Displaying the micro time as a string :0.62248800 1620222618
```
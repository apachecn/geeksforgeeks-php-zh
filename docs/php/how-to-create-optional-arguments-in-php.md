# 如何在 PHP 中创建可选参数？

> 原文:[https://www . geesforgeks . org/how-create-optional-arguments-in-PHP/](https://www.geeksforgeeks.org/how-to-create-optional-arguments-in-php/)

即使没有传递给函数，也不会停止函数工作的参数称为可选参数。参数的存在是完全可选的，如果提供了，它们的值将被程序接受。但是如果某个参数没有赋值，程序就不会停止。这些参数通常是通过为函数提供参数的默认值而产生的。现在，如果函数在调用过程中被赋予了参数值，那么给定的参数将覆盖默认参数，程序将正常继续。但是如果调用没有给函数提供任何值，程序会正常地继续默认的值。

这里的想法是在程序中创建这样的可选参数。如上所述，这将使用默认值来执行。

**流程图:**虽然概念挺直截了当但这里有个流程图更好理解。
T3】

下面的例子说明了 PHP 中的可选参数。

**例 1:**

```php
<?php
function travel($place = "Sweden")
{
  return "Traveling to $place.\n";
}
echo travel();
echo travel("Australia");
echo travel("Tokyo");
?>
```

**输出:**

```php
Travelling to Sweden. 
Traveling to Australia. 
Traveling to Tokyo.
```

**示例 2:** 在本示例中，它确认定时器已设置。

```php
<?php
function timer($hour=00, $min=00, $sec=00)
{ 
  $time="$hour : $min : $sec.";
  return "Timer set for $time \n";
}
echo timer();
echo timer(10, 30, );
echo timer(00, 20, 40);
?>
```

**输出:**

```php
Timer set for 0 : 0 : 0\. 
Timer set for 10 : 30 : 0\. 
Timer set for 0 : 20 : 40.
```
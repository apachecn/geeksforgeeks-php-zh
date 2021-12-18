# 如何在 PHP 中将字符串转换成数字？

> 原文:[https://www . geesforgeks . org/如何将字符串转换为 php 中的数字/](https://www.geeksforgeeks.org/how-to-convert-a-string-into-number-in-php/)

PHP 中的字符串可以非常容易地转换成数字(浮点/ int / double)。在大多数用例中，它不是必需的，因为 PHP 做隐式类型转换。在 PHP 中将字符串转换成数字的方法有很多，下面讨论其中的一些:

**方法 1** :使用 [number_format()函数](https://www.geeksforgeeks.org/php-number_format-function/)。number_format()函数用于将字符串转换为数字。它在成功时返回格式化的数字，否则在失败时给出 E_WARNING。

**例:**

```
<?php

$num = "1000.314";

// Convert string in number using 
// number_format(), function
echo number_format($num), "\n";

// Convert string in number using 
// number_format(), function
echo number_format($num, 2);
?>
```

**输出:**

```
1,000
1,000.31

```

**方法二:使用类型转换:**类型转换可以直接将字符串转换为 float、double 或 integer 基元类型。这是在没有任何函数的情况下将字符串转换为数字的最佳方式。

**例:**

```
<?php

// Number in string format
$num = "1000.314";

// Type cast using int
echo (int)$num, "\n";

// Type cast using float
echo (float)$num, "\n";

// Type cast using double
echo (double)$num;
?>
```

**输出:**

```
1000
1000.314
1000.314

```

**方法 3** :使用 [intval()](https://www.geeksforgeeks.org/php-intval-function/) 和 [floatval()](https://www.geeksforgeeks.org/php-floatval-function/) 功能。intval()和 floatval()函数也可用于将字符串分别转换为相应的整数值和浮点值。

**例:**

```
<?php

// Number in string format
$num = "1000.314";

// intval() function to convert 
// string into integer
echo intval($num), "\n";

// floatval() function to convert
// string to float
echo floatval($num);
?>
```

**输出:**

```
1000
1000.314

```

**方法 4** :加 0 或进行数学运算。通过将 0 与字符串相加，也可以将字符串数字转换为整数或浮点数。在 PHP 中，执行数学运算时，字符串被隐式转换为整数或浮点数。

```
<?php

// Number into string format
$num = "1000.314";

// Performing mathematical operation 
// to implicitly type conversion
echo $num + 0, "\n";

// Performing mathematical operation 
// to implicitly type conversion
echo $num + 0.0, "\n";

// Performing mathematical operation 
// to implicitly type conversion
echo $num + 0.1;
?>
```

**输出:**

```
1000.314
1000.314
1000.414

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。
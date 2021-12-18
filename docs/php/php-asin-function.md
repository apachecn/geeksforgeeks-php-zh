# PHP | asin()函数

> 原文:[https://www.geeksforgeeks.org/php-asin-function/](https://www.geeksforgeeks.org/php-asin-function/)

三角学是数学的重要组成部分，PHP 的数学函数为我们提供了一些对涉及三角学的计算非常有用的函数。其中一个函数就是 asin()函数。PHP 中的 *asin()* 函数用来求一个以弧度为单位的数的反正弦。
我们已经讨论过 [PHP | sin()函数](https://www.geeksforgeeks.org/php-sin-function/)了。asin()函数是 sin()的互补函数。
在 asin()函数中传递的参数应该指定一个范围在-1 到 1 之间的数字。

**语法:**

```php
*float* asin($value)
```

**参数:**该函数接受单个参数$值。它是您想要查找其反正弦值的数字。此参数的值必须以弧度为单位。

**返回值:**返回一个浮点数，它是作为参数传递给它的数字的反正弦值。

示例:

```php
Input : asin(0)
Output : 0

Input : asin(1)
Output : 1.5707963267949

Input : asin(-1)
Output : -1.5707963267949

Input : asin(2)
Output : NaN

```

下面的程序说明了 PHP 中的 asin()函数:

*   Passing 0 as a parameter:

    ```php
    <?php

    echo (asin(0));

    ?>      
    ```

    输出:

    ```php
    0
    ```

*   Passing 1 as a parameter:

    ```php
    <?php

    echo (asin(1));

    ?>      
    ```

    输出:

    ```php
    1.5707963267949
    ```

*   Passing -1 as a parameter:

    ```php
    <?php

    echo (asin(-1));

    ?>      
    ```

    输出:

    ```php
    -1.5707963267949
    ```

*   Passing 2 as a parameter:

    ```php
    <?php

    echo (asin(2));

    ?>      
    ```

    输出:

    ```php
    NaN
    ```

**参考**:
T3】http://php.net/manual/en/function.asin.php
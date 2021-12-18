# PHP | cos()函数

> 原文:[https://www.geeksforgeeks.org/php-cos-function/](https://www.geeksforgeeks.org/php-cos-function/)

三角学是数学的重要组成部分，PHP 的数学函数为我们提供了一些对涉及三角学的计算非常有用的函数。PHP 中的 *cos()* 函数用来求一个数的余弦。
cos()函数返回一个介于-1 和 1 之间的浮点值，代表角度的余弦值。传递给它的参数必须以弧度为单位。

**语法:**

```php
*float* cos($value)
```

**参数:**该功能接受单个参数*值*。它是你想求余弦的数字。该值必须以弧度为单位。

**返回值:**返回一个浮点数，它是作为参数传递给它的数字的余弦值。

示例:

```php
Input : cos(3) 
Output : -0.98999249660045

Input : cos(-3)
Output : -0.98999249660045

Input : cos(2*M_PI)
Output : 1

Input : cos(0) 
Output : 1

```

下面的程序说明了 PHP 中的 cos()函数:

*   Passing 3 as a parameter:

    ```php
    <?php

    echo (cos(3));

    ?>      
    ```

    输出:

    ```php
    -0.98999249660045
    ```

*   Passing -3 as a parameter:

    ```php
    <?php

    echo (cos(-3));

    ?>      
    ```

    输出:

    ```php
    -0.98999249660045
    ```

*   When (2*M_PI) is passed as a parameter, M_PI is a constant in PHP whose value is 3.1415926535898:

    ```php
    <?php

    echo (cos(2*M_PI));

    ?>      
    ```

    输出:

    ```php
    1
    ```

*   Passing 0 as a parameter:

    ```php
    <?php

    echo (cos(0));

    ?>      
    ```

    输出:

    ```php
    1
    ```

**参考**:
T3】http://php.net/manual/en/function.cos.php
# PHP | atan2()函数

> 原文:[https://www.geeksforgeeks.org/php-atan2-function/](https://www.geeksforgeeks.org/php-atan2-function/)

*atan2()* 函数是 PHP 中的内置函数，用于计算作为参数传递给它的两个变量 x 和 y 的反正切。
该函数以弧度为单位返回结果，弧度介于-π和π(含)之间。

**语法:**

```php
*float* atan2($y, $x)
```

**参数:**该功能接受两个参数，描述如下:

1.  **$y:** 此参数指定分红。
2.  **$x:** 此参数指定除数。

**返回值:**返回一个浮点值，它是 y/x 的反正切，单位为弧度。

示例:

```php
Input : atan2(0.50, 0.50)
Output : 0.78539816339745

Input : atan2(-0.50, -0.50)
Output : -2.3561944901923

Input : atan2(5, 5) 
Output : 0.78539816339745

Input : atan2(10, 20) 
Output : 0.46364760900081

```

下面的程序，取不同的参数值用来说明 PHP 中的 atan2()函数:

*   When (0.50, 0.50) is passed as a parameter:

    ```php
    <?php

    echo (atan2(0.50, 0.50));

    ?>      
    ```

    输出:

    ```php
    0.78539816339745
    ```

*   When (-0.50, -0.50) is passed as a parameter:

    ```php
    <?php

    echo (atan2(-0.50, -0.50));

    ?>      
    ```

    输出:

    ```php
    -2.3561944901923
    ```

*   When (5, 5) is passed as a parameter:

    ```php
    <?php

    echo (atan2(5, 5));

    ?>      
    ```

    输出:

    ```php
    0.78539816339745
    ```

*   When (10, 20) is passed as a parameter:

    ```php
    <?php

    echo (atan2(10, 20));

    ?>      
    ```

    输出:

    ```php
    0.46364760900081
    ```

    **参考**:
    T3】http://php.net/manual/en/function.atan2.php
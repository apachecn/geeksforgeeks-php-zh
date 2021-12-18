# PHP|pi()函数

> Original: [https://www.geeksforgeeks.org/php-pi-function/](https://www.geeksforgeeks.org/php-pi-function/)

在解决数学问题时，我们经常会遇到需要π值的问题。 手动插入 PI(π)的值可能既耗时又错误。 它也不被认为是一种好的编程实践。 为了解决这个问题，PHP pi()的内置函数提供了帮助。

Php 中的 pi()函数用于返回π的值。 此外，M_Pi 是一个命名常量 PHP，它给出的值与 pi()函数返回的值相同。 它比 pi()函数稍微快一些。

与π相关的其他一些预定义命名常量包括：

*   **M_PI_2：**描述π/2，取值为 1.570796。
*   **M_PI_4：**描述π/4，取值为 0.785398。
*   **M_1_PI：**描述 1/π。 它的价值是 0.318309。
*   **M_Pi：**它描述π。 它的价值是 3.141592。
*   **M_2_PI：**描述 2/π。 它的价值是 0.636619。
*   **M_SQRTPI：**它描述 SQRT(π)。 它的价值是 1.772453。
*   **M_2_SQRTPI：**它描述 2/SQRT(π)。 它的价值是 1.128379。

**语法：**

```php
*float* pi()
```

**参数**：此函数不接受任何参数。

**返回值：**返回一个浮点值，它是 PI 的近似值。

例如：

```php
Input : echo(pi())
Output : 3.1415926535898

Input : echo M_PI
Output : 3.1415926535898

```

下面的程序演示了 PHP 中的 pi()函数：

1.  When pi() function is used:

    ```php
    <?php

    echo(pi());

    ?>
    ```

    产出：

    ```php
    3.1415926535898
    ```

2.  When M_PI is used for finding the value of PI:

    ```php
    <?php

    echo M_PI;

    ?>
    ```

    产出：

    ```php
    3.1415926535898
    ```

**重要注意事项：**

*   函数的作用是：返回π的值。
*   M_Pi 是一个命名常量，它比 pi()函数稍微快一些。
*   Pi()函数以浮点数形式返回 pi 的值。

**参考**：
[http://php.net/manual/en/function.pi.php](http://php.net/manual/en/function.pi.php)
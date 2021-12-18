# PHP | array_product()函数

> 原文:[https://www.geeksforgeeks.org/php-array_product-function/](https://www.geeksforgeeks.org/php-array_product-function/)

有些时候我们需要计算一个数组中所有元素的乘积。最基本的方法是迭代所有元素并计算乘积，但是 PHP 为我们提供了一个内置函数来完成这个任务。array_product()是 PHP 中的内置函数，用于查找数组中所有元素的乘积。

**语法:**

```
array_product($array)
```

**参数:**函数只取一个参数 **$array** ，指的是我们希望得到其元素乘积的输入数组。

**返回值:**array _ product()函数根据数组元素的性质返回一个整数或浮点值。

**示例:**

```
Input : array = (5, 8, 9, 2, 1, 3, 6)
Output : 12960

Input : array = (3.2, 4.8, 9.1, 4.36, 1.14)
Output : 694.7426304

```

下面的程序说明了 array_product()函数的工作原理:

*   When the array passed to the array_product() function contains only integral values then the array_product() function returns an integer value equals to the product of all the elements of the array passed to it.

    ```
    <?php

    // PHP function to illustrate the use 
    // of array_product()

    // Return Integer number
    function Product($array)
    {
        $result = array_product($array);
        return($result);
    }

    $array = array(5, 8, 9, 2, 1, 3, 6);
    print_r(Product($array));
    ?>
    ```

    输出:

    ```
    12960

    ```

*   When the array passed to the array_product() function contains both integral and float values then the array_product() function returns a floating point value equals to the product of all the elements of the array passed to it.

    ```
    <?php
    // PHP function to illustrate the use of
    // array_product()
    function Product($array)
    {
        $result = array_product($array);
        return($result);
    }

    $array = array(3.2, 4.8, 9.1, 4.36, 1.14);
    print_r(Product($array));
    ?>
    ```

    输出:

    ```
    694.7426304

    ```

**参考**:
T3】http://php.net/manual/en/function.array-product.php
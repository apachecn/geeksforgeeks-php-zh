# PHP|数据类型

> Original: [https://www.geeksforgeeks.org/php-data-types/](https://www.geeksforgeeks.org/php-data-types/)

数据类型定义变量可以存储的数据类型。 PHP 允许八种不同类型的数据类型。 所有这些都将在下面讨论。 有预定义的、用户定义的和特殊的数据类型。

预定义的数据类型包括：

*   布尔代数学（或逻辑）体系的
*   整数 / 完整物 / 统一体
*   两倍物 / 成对物 / 两倍 / 双精度型
*   细绳

用户定义(复合)数据类型包括：

*   有序的安排 / 排列 / 大批
*   东西 / 对象 / 目标 / 物体

特殊数据类型包括：

*   无约束力的 / 无效的
*   资源 / 出路 / 应付办法 / 办法

前五种称为简单数据类型，后三种称为复合数据类型：

1.  **Integer**：整数只包含包括正数和负数的整数，即没有小数部分或小数点的数字。 它们可以是十进制(基数 10)、八进制(基数 8)或十六进制(基数 16)。 默认基数为小数(基数为 10)。 八进制整数可以用前导 0 声明，十六进制可以用前导 0x 声明。 整数范围必须在-2^31 到 2^31 之间。
    **示例：**

    ## PHP

    ```
    <?php

    // decimal base integers
    $deci1 = 50; 
    $deci2 = 654; 

    // octal base integers
    $octal1 = 07; 

    // hexadecimal base integers
    $octal = 0x45; 

    $sum = $deci1 + $deci2;
    echo $sum;

    ?>
    ```

    **输出：**
    和

    ```
    704
    ```

2.  **Double**: Can hold numbers containing fractional or decimal parts including positive and negative numbers or a number in exponential form. By default, the variables add a minimum number of decimal places. The Double data type is the same as a float as floating-point numbers or real numbers.

    **示例：**

    ## PHP

    ```
    <?php

    $val1 = 50.85; 
    $val2 = 654.26; 

    $sum = $val1 + $val2;

    echo $sum;

    ?>
    ```

    **Output: **

    ```
    705.11
    ```

3.  **字符串**：包含字母或任意字母，包含偶数。 这些都是在申报过程中用双引号括起来的。 字符串也可以用单引号括起来，但在打印变量时会有不同的处理方式。 为了阐明这一点，请看下面的示例。[
    **示例：**
    和

    ## PHP

    ```
    <?php

    $name = "Krishna";
    echo "The name of the Geek is $name \n";
    echo 'The name of the geek is $name';

    ?>
    ```

    **输出：**

    ```
    The name of the Geek is Krishna 
    The name of the geek is $name
    ```

4.  **NULL**: These are special types of variables that can hold only one value i.e., NULL. We follow the convention of writing it in capital form, but it’s case-sensitive. If a variable is created without a value or no value, it is automatically assigned a value of NULL. It is written in capital letters.

    **示例：**

    ## PHP

    ```
    <?php

    $nm = NULL;
    echo $nm;    // This will give no output

    ?>
    ```

5.  **布尔**：在条件测试中使用布尔数据类型。 仅保留两个值，TRUE(1)或 FALSE(0)。 成功的事件将返回*TRUE*，不成功的事件将返回*FALSE。* 在布尔值中，NULL 类型值也被视为*FALSE*。 除了 NULL 之外，0 在布尔值中也被认为是 FALSE。 如果字符串为空，则它在布尔数据类型中也被视为 FALSE。
    示例：
    和

    ## PHP

```
<?php

if(TRUE)
    echo "This condition is TRUE";
if(FALSE)
    echo "This condition is not TRUE";
?>
```
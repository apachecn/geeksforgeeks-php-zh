# PHP money_format()函数

> Original: [https://www.geeksforgeeks.org/php-money_format-function/](https://www.geeksforgeeks.org/php-money_format-function/)

**Money_Format()**函数是 PHP 中的一个内置函数，它返回一个格式为货币字符串的数字。 在主字符串中，格式化的数字插入有百分号(%)的位置。
该函数仅在具有**strfmon()**容量的系统中定义。 例如，Windows 中没有定义**Money_Format()**。 它主要与另一个预定义的 PHP 函数**setlocale()**配合使用，其区域设置类别为**LC_MULNCY**。 从 7.4 版开始，**Money_Format()**已弃用。 相反，使用**NumberForMatter：：FormatCurrency()**。

**语法：**

```php
*string* money_format( *string* str, *float* num )
```

**示例：**

```php

money_format("you have to pay %i", $num);

```

**返回值：**它返回格式化字符串。 它将返回格式字符串前后未更改的字符。

**参数：**

**str：**它指定要格式化的字符串以及其中变量的格式化方式。 字符串参数由下一个序列组成。

1.  **%字符**在主字符串中插入格式化的数字。
2.  **可选标志**可以使用一个或多个后续标志。
    *   **=f**数字填充字符。 默认填充字符为空格。
    *   **^**禁用分组字符。
    *   **+或**指定正数和负数的格式样式。 如果使用+，则将使用+和-的区域设置等效项。 负数用括号括起来。 默认情况下，除非提到数字的符号，否则该特征为+。(请参阅示例 2)
    *   **！**取消输出字符串中的货币符号。
    *   **-**如果存在，它会使所有字段左对齐(向右填充)，这与默认值不同，默认情况下，字段是右对齐(向左填充)。
3.  **宽度**
    *   **w**指定最小字段宽度的十进制数字字符串，除非使用标志，否则该最小字段宽度将右
        对齐。 其默认值为 0(零)。
4.  **可选左精度**
    *   **#n**这用于定义数字的刻度(小数点左边的最大位数(N))。 如果位数小于 n，它用于通过使用填充字符保持格式化输出在同一列中对齐。如果位数大于 n，则忽略此规范。如果未使用^标志，则在添加填充字符(如果有)之前插入分组分隔符。 如果填充字符是数字，分组分隔符将不会应用于填充字符。 格式化输出中出现在数字之前或之后的任何字符都会根据需要用空格字符填充，以确保正确对齐。
5.  **可选的右精度**
    *   **.p**小数点后紧跟另一个(P)位数。 如果 p 为 0，则将省略小数字符及其右侧的数字。 如果没有提到正确的精度，则默认设置将由当前使用的区域设置决定。 在格式化过程之前，要格式化的金额将舍入到指定的位数。
6.  **必需的转换字符**
    *   **i**根据区域设置国际货币格式设置数字格式。
    *   **n**根据区域设置国家货币格式设置数字格式。
    *   **%**返回%CHARACTER。

**数字：**要格式化的数字。

**示例 1：**此示例以其区域设置国际和国家格式打印给定的数字。

```php
<?php

$num = 8456.22;

setlocale(LC_MONETARY, "en_US");

echo money_format("The output in locales"
    . " international format is %i", $num);
echo "\n";

echo money_format("The output in locales"
    . " national format is %n", $num);
?>
```

发帖主题：Re：Колибри0.7.0

```php
The output in locales international format is USD 8, 456.22 
The output in locales national format is $8, 456.22

```

**示例 2：**接受负数并将其显示为货币的程序。

```php
<?php

$num = -8456.22;
setlocale(LC_MONETARY, "en_US");
echo money_format("output: %(n", $num);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Output: ($8, 456.22)
```
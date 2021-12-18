# PHP|setlocale()函数

> Original: [https://www.geeksforgeeks.org/php-setlocale-function/](https://www.geeksforgeeks.org/php-setlocale-function/)

Setlocale()函数是 PHP 中的内置函数，用于设置区域设置信息。 区域设置意味着为您的系统分配一个地理位置，然后根据该位置的区域设置执行某些功能。 通常，处理其他地方的日期和时间的程序会处理这个问题。
**语法：**和

```
setlocale( $category , $locale )
```

**返回值：**它返回新的当前区域设置，如果您的平台上未实现区域设置功能、指定的区域设置不存在或类别名称无效，则返回 False。
**参数：**此函数接受上述两个参数，如下所述：

*   **类别：**它是一个名为常量的整数，指定受区域设置影响的函数类别：
    *   **LC_ALL**-适用于以下所有内容
    *   **LC_COLLATE**-用于字符串比较
    *   **LC_CTYPE**-用于字符分类和转换
    *   **LC_MICRICAL**-用于 localeconv()
    *   **LC_NUMBER**-用于小数分隔符
    *   **LC_TIME**-用于使用 strftime()格式化日期和时间
    *   **LC_Messages**-用于系统响应
*   **区域设置：**通常是指定地区所需的区域设置数组。
    *   如果区域设置为 NULL 或空字符串-区域设置名称将从与上述类别同名的环境变量的值或从“lang”设置。
    *   如果区域设置为“0”-区域设置不受影响，则只返回当前设置。
    *   如果区域设置是数组-区域设置不受影响，则只返回当前设置。

下面的示例说明 PHP 中的**setlocale()函数**：
**示例 1：**生成区域设置定义时间的简单程序。

## PHP

```
<?php

// Setting locale to german
setlocale(LC_ALL,"de");
echo strftime("The current german time is %r");

// Setting locale to english
setlocale(LC_ALL,"en");
echo strftime(" and the current english time is %r");
?>
```

发帖主题：Re：Колибри0.7.8.0

```
The current german time is 08:17:45 AM 
and the current english time is 08:17:45 AM
```

**示例 2：**检查系统支持哪个德语区域设置名称的程序。

## PHP

```
<?php

// Try different possible locale names for german
$loc_de = setlocale(LC_ALL, 'de_DE@euro', 'de_DE', 'deu_deu');
echo "Preferred locale for german on this system is '$loc_de'";
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Preferred locale for german on this system is 'German_Germany.1252'
```

**示例 3：**使用 LC_MULNCY 命令的简单程序

## PHP

```
<?php

// Setting locale to english
setlocale(LC_MONETARY,"en");
$loc=localeconv();
print_r($loc);
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Array
(
    [decimal_point] => .
    [thousands_sep] => 
    [int_curr_symbol] => 
    [currency_symbol] => 
    [mon_decimal_point] => 
    [mon_thousands_sep] => 
    [positive_sign] => 
    [negative_sign] => 
    [int_frac_digits] => 127
    [frac_digits] => 127
    [p_cs_precedes] => 127
    [p_sep_by_space] => 127
    [n_cs_precedes] => 127
    [n_sep_by_space] => 127
    [p_sign_posn] => 127
    [n_sign_posn] => 127
    [grouping] => Array
        (
        )

    [mon_grouping] => Array
        (
        )

)
```

**引用：**[https://www.php.net/manual/en/function.setlocale.php](https://www.php.net/manual/en/function.setlocale.php)和
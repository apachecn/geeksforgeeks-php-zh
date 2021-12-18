# PHP|IntlChar 枚举 CharNames()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-enumcharnames-function/](https://www.geeksforgeeks.org/php-intlchar-enumcharnames-function/)

**IntlChar：：枚举 CharNames()**函数是 PHP 中的一个内置函数，用于给出一个范围内所有可用赋值 Unicode 字符的目录。 该列表将包含起始代码点(包括起始代码点)和限制代码点(不包括限制代码点)之间的 Unicode 字符。 将为每个函数调用一个函数，并将代码点值与字符名称一起传递。 那些与新的&现代名称不同的名称，对于 Unicode 1.0 名称，只有那些名称将被编目。
**语法：**

```
*void* IntlChar::enumCharNames( $start, $limit, $callback,
$nameChoice = IntlChar::UNICODE_CHAR_NAME )  
```

**参数：**此函数接受四个参数，如下所述：

*   **开始：**此参数保存枚举范围内的第一个代码点。
*   **限制：**此参数保存的值比范围内的最后一个点多一个。
*   **回调：**对于每个字符名称，应该调用的函数。 此函数接受下面列出的三个参数：
    *   **$codepoint：**它保存数字代码点的值。
    *   **$nameChoice：**它保存 nameChoice 的值。
    *   **$name：**它保存角色的名称。
*   **nameChoice：**必须枚举的名称类型。 它可以是以下五个给定常量中的任何一个：
    *   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
    *   IntlChar：：CHAR_NAME_ALIAS
    *   IntlChar：：CHAR_NAME_CHOICE_COUNT
    *   IntlChar：：Extended_Char_
    *   IntlChar：：UNICODE_10_CHAR_NAME

**返回值：**此函数不返回任何值。
下面的程序说明了 PHP：
**程序：**中的**IntlChar：：EumpCharNames()**函数

## PHP

```
<?php

// PHP program to uses IntlChar::enumCharNames()
// function
IntlChar::enumCharNames(0x2700, 0x2710,
    function($codepoint, $nameChoice, $name) {
        printf("U+%04x %s\n", $codepoint, $name);
});

?>
```

发帖主题：Re：Колибри0.7.0

```
U+2700 BLACK SAFETY SCISSORS
U+2701 UPPER BLADE SCISSORS
U+2702 BLACK SCISSORS
U+2703 LOWER BLADE SCISSORS
U+2704 WHITE SCISSORS
U+2705 WHITE HEAVY CHECK MARK
U+2706 TELEPHONE LOCATION SIGN
U+2707 TAPE DRIVE
U+2708 AIRPLANE
U+2709 ENVELOPE
U+270a RAISED FIRST
U+270b RAISED HAND
U+270c VICTORY HAND
U+270d WRITING HAND
U+270e LOWER RIGHT PENCIL
U+270f PENCIL
```

**引用：**[https://www.php.net/manual/en/intlchar.enumcharnames.php](https://www.php.net/manual/en/intlchar.enumcharnames.php)
# PHP|格式说明符

> Original: [https://www.geeksforgeeks.org/php-format-specifiers/](https://www.geeksforgeeks.org/php-format-specifiers/)

字符串可以说是最常用的数据类型之一，与编程语言无关。 字符串可以是硬编码的(由开发人员直接指定)，也可以是格式化的(其中指定了基本框架，最后的字符串是通过合并其他变量的值获得的)。 格式化字符串可以定义为一组段，其中每个段可以包含整数、浮点数或甚至另一个字符串。

格式化字符串使用格式说明符创建字符串的基本结构。 格式说明符是预定义的字符序列，可用于定义要存储或显示的数据类型以及任何给定值应如何格式化，即精度、填充等。格式说明符通常以百分位符号或‘%’开头，后跟定义数据类型和所需格式的字符序列。 当迭代一种格式时，如果遇到任何格式说明符，编译器/解释器都会理解，存在一个相应的指令，其值将被格式化并使用。 **因此，字符串可能根本不包含格式说明符，但如果它包含格式说明符，则至少应该重新发送相同数量的指令。 在指令过多的情况下，一些语言会忽略不需要的指令，并让它在发出警告的情况下执行。**

下面简要讨论可以在 PHP 中指定的格式和数据类型。 它们中的每一个都使用前面的百分位符号或‘%’来实现。

**格式化值**

*   **符号说明符**可用于强制显示要在数字上使用的符号(-或+)。 默认情况下，只有-号显示在负数上。 使用此说明符，正数将与前面的+一起显示。 这可以使用+符号来实现，并且只能在数值上实现。 示例，

    ```php
    %+d    // Specify the integer along with it's sign (+ or -).

    ```

*   **填充说明符**可用于指定将使用哪个字符将结果填充到任何定义的字符串大小。 默认情况下，空格用作填充。 可以通过单引号或‘作为前缀来指定备用填充字符。 示例，

    ```php
    %'0d    // Pad with 0s to achieve the right length. 

    ```

*   **对齐说明符**可用于指定结果的对齐方式，即左对齐还是右对齐。 默认情况下，它是右对齐的。 使用-字符使其左对齐。 示例，

    ```php
    %-s    // Specifies the alignment as left-justified.

    ```

*   **宽度说明符**可用于指定结果本身中出现的最小字符数。 它可以使用表示最小宽度的任何数字来指定。 它最常与填充说明符一起使用。 示例，

    ```php
             // Specifies there should be at least 5 digits,
    %'05d    // if less, then 0s are filled to get the desired result.  

    ```

*   **精度说明符**可用于在处理实数时指定精度。 句号或‘’ 后跟一个可选的十进制数字字符串，该字符串表示要在小数点后显示的小数位数。
    在字符串上使用此说明符时，它指定字符串的最大字符限制。
    例如，

```php
%.5f    // Defines Real Number Precision.
%.2s    // Maximum Character to be allowed in a string.  

```

**数据类型**

*   %：显示%。 不需要指令。
*   B：该指令引用整数，并显示为二进制数。
*   C：该指令引用一个整数，并显示为相应的 ASCII 字符。
*   D：该指令引用整数，并显示为十进制数。
*   E：该指令指的是科学记数法(例如 2.12E+3)。
*   E：也就是圣人抯的别名。
*   F：该指令引用浮点数并显示为实数(区域感知)。
*   F：该指令引用浮点数并显示为实数(不支持区域设置)。
*   O：该指令引用整数，并显示为八进制数。
*   S：该指令被视为字符串并显示为字符串。
*   U：该指令引用整数，并显示为无符号十进制数字。
*   X：该指令引用一个整数，并显示为十六进制数字(带有小写字母)。
*   X：该指令引用一个整数，并显示为十六进制数字(大写字母)。

下面的代码说明了不同格式说明符的工作方式：

```php
<?php

// PHP program to illustrate Working 
// of different Format Specifiers

// Creating Dummy Variables 
$numValue = 5;
$strValue = "GeeksForGeeks";

// Using Sign Specifier.
printf("Signed Number: %+d\n",$numValue);

// Padding and Width Specifier.
printf("Padding and Width\n%'03d\n%'03d\n",
                    $numValue,$numValue+10);

// Precision Specifier.
printf("Precision: %.5f %.5s\n", $numValue, $strValue);

// Different DataTypes.
// Integer and Percentile.
printf("Percentage: %d%%\n",$numValue);

// Binary Octal and Hexadecimal Representation.
printf("Binary: %b Octal: %o Hexadecimal: %x\n",
        $numValue+10,$numValue+10,$numValue+10);

// Character Representation.
printf("Character: %c\n",$numValue+60);

// Strings.
printf("String: %s\n",$strValue);

// Real Numbers.
printf("RealNumber: %f\n",1/$numValue); 

// Scientific Numerical Representation.
printf("Scientific Representation:%e\n",$numValue+100); 

?>
```

产出：

```php
Signed Number: +5
Padding and Width
005
015
Precision: 5.00000 Geeks
Percentage: 5%
Binary: 1111 Octal: 17 Hexadecimal: f
Character: A
String: GeeksForGeeks
RealNumber: 0.200000
Scientific Representation:1.050000e+2

```
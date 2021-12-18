# PHP|substr_place()函数

> Original: [https://www.geeksforgeeks.org/php-substr_replace-function/](https://www.geeksforgeeks.org/php-substr_replace-function/)

substr_place()函数是 PHP 中的内置函数，用于将一个字符串的一部分替换为另一个字符串。 需要将原始字符串中要执行替换的索引作为参数传递。 如果需要，还可以指定更换的长度。 字符串数组可以作为此函数的参数提供，在这种情况下，替换将依次发生在每个字符串上。

**语法：**

```
substr_replace($string, $replacement, $start, $length)
```

**参数：**此函数接受四个参数，如上面的语法所示，其中前三个参数是必需的，最后一个参数是可选的。 所有这些参数如下所述：

*   **$string：**此参数是必需的。 它指定要在其中进行替换的输入字符串。
*   **$Replace：**此参数也是必需的。 它指定要插入$string 中的字符串。
*   **$START：**此参数也是必需的。 它指定需要开始更换的位置。
    *   如果$START 是**正数**，则替换从字符串中的指定位置开始
    *   如果$start 是**负数**，则从字符串的**结尾**的指定位置开始替换
    *   如果$START 为 0，则从字符串的第一个字符开始替换
*   **$Length：**此参数是可选的。 它指定应该替换多少个字符。 如果未指定$LENGTH，则替换将在$STRING 的末尾停止
    *   如果$Length 为**正**，则表示要替换的$STRING 部分的长度。
    *   如果$Length 为**负**，则表示从$string 末尾开始需要停止替换的字符数。
    *   如果$Length 为 0，则执行插入而不是替换。

**返回值：**返回替换后生成的字符串。 如果是字符串数组，则返回该数组。

例如：

```
Input : $string = "Geeks for Geeks", $replacement = "GFG", $start = 0
Output : GFG

Input : $string = "Hello World", $replacement = "Hello", $start = 6
Output : Hello Hello

```

下面的程序演示了 substr_place()函数：

**程序 1：**在此程序中，我们将使用不带任何$Length 参数的 substr_place()函数。 从$START 到$STRING 结尾的所有字符都将替换为$REPLACE。

```
<?php

echo substr_replace("Hello World", "GFG", 6);

?>
```

输出

```
Hello GFG
```

**程序 2：**在此程序中，我们将使用$length 设置为 0 的 substr_place()函数。 在这种情况下，将发生插入。 不会进行任何替换。

```
<?php

echo substr_replace("Contribute GFG", "to ", 11, 0);

?>
```

输出

```
Contribute to GFG
```

**程序 3：**在此程序中，我们将使用 substr_place()函数，并将$length 设置为正值。 在这种情况下，$替换字符串将替换$START 中最多$LENGTH 的$STRING 字符。

```
<?php

echo substr_replace("alone", "ph", 0, 2);

?>
```

输出

```
phone
```

**程序 4：**在此程序中，我们将使用 substr_place()函数，并将$length 设置为负值。 在这种情况下，$替换字符串将替换$STRING 中$START 的字符，并在从字符串末尾开始的$LENGTH 字符数之前停止。

```
<?php

echo substr_replace("alone", "ph", 0, -3);

?>
```

输出

```
phone
```

**程序 5：**在此程序中，我们将使用 substr_place()函数，不带任何$length 参数，并将$start 设置为负值。 替换将从字符串末尾的指定位置开始。

```
<?php

echo substr_replace("alpha", "one", -3);

?>
```

输出

```
alone
```

**引用：**[http://php.net/manual/en/function.substr-replace.php](http://php.net/manual/en/function.substr-replace.php)
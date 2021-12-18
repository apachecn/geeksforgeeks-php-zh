# PHP 中“break”或“continue”语句后的数字有什么用？

> 原文:[https://www . geeksforgeeks . org/什么是在 php 中使用中断或继续语句后使用数字/](https://www.geeksforgeeks.org/what-is-the-use-of-number-after-break-or-continue-statements-in-php/)

中断和继续是用于控制循环中迭代的两个关键词。这两个关键字之间的主要区别是“break”用于终止循环，而“continue”跳过当前迭代。为了理解“break”和“continue”关键词后写的数字的含义，让我们首先借助例子理解基本的“break”和“continue”。

**例 1:** 本例描述了不带编号的“break”关键字。

```php
<?php

$i = 0;

for ($i = 0; $i <= 5; $i++) {
    if ($i == 4) {
        break;
    }
    echo $i . " ";
}

?>
```

**输出:**

```php
0 1 2 3 
```

**例 2:** 本例描述了不带编号的“continue”关键字。

```php
<?php

$i = 0;

for ($i = 0; $i <= 5; $i++) {
    if ($i == 3) {
        continue;
    }
    echo $i . " ";
}
?>
```

**输出:**

```php
0 1 2 4 5
```

现在，我们精通“中断”和“继续”关键词，所以让我们理解这些用数字写的关键词。带有关键字的数字描述了有多少嵌套语句将受到影响。例如，对于具有两个嵌套循环的代码，在内部循环中写入*中断 2* 以中断两个循环的执行。借助于以下代码，已经描述了相同的情况。

**例 3:** 本例用数字描述“break”关键字。

```php
<?php

$numbers = array(4, 6, 8);
$letters = array("X", "Y", "Z");

foreach ($numbers as $num) {
    foreach ($letters as $char){
        if ($char == "Z") {
            break 2; 
        }
        echo $char;
    }
    echo $num;
}
?>
```

**输出:**

```php
XY
```

**例 4:** 本例用数字描述“continue”关键字。

```php
<?php

$numbers = array(6, 8, 10);
$letters = array("X", "Y", "Z");

foreach ($numbers as $num) {
    foreach ($letters as $char) {
        if ($char == "Z") {
            continue 2;
        }
        echo $char;
    }
    echo $num;
}
?>
```

**输出:**

```php
XYXYXY
```
# PHP|Gmagick queryfontmetrics()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-queryfontmetrics-function/](https://www.geeksforgeeks.org/php-gmagick-queryfontmetrics-function/)

**Gmagick：：queryfontmetrics()函数**是 PHP 中的内置函数，它返回一个数组，该数组表示包含 characterWidth、characterHeight、ascender、downender、textWidth、textHeight 和 maxumHorizontalAdvance 的字体度量。

**语法：**

```
*Gmagick* Gmagick::queryfontmetrics( *GmagickDraw* $draw, *string* $text )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Draw：**它指定 GmagickDraw 对象。
*   **$text：**它指定文本。

**返回值：**成功时，此函数返回包含指标的数组。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：queryfontmetrics()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(参见默认字体规格)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Get the metrics
$fontMetrics = $gmagick->queryfontmetrics($draw, 'Hello');
print("<pre>" . print_r($fontMetrics, true) . "</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [characterWidth] => 12
    [characterHeight] => 12
    [ascender] => 12
    [descender] => -4
    [textWidth] => 29
    [textHeight] => 15
    [maximumHorizontalAdvance] => 13
)
```

**程序 2(参见本地字体文件规格)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Use a local font file
$draw->setfont('Pacifico.ttf');

// Get the metrics
$fontMetrics = $gmagick->queryfontmetrics($draw, 'Hello');
print("<pre>" . print_r($fontMetrics, true) . "</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [characterWidth] => 12
    [characterHeight] => 12
    [ascender] => 17
    [descender] => -6
    [textWidth] => 28
    [textHeight] => 22
    [maximumHorizontalAdvance] => 19
)
```

**引用：**[https://www.php.net/manual/en/gmagick.queryfontmetrics.php](https://www.php.net/manual/en/gmagick.queryfontmetrics.php)
# PHP|GmagickPixel getcolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickpixel-getcolor-function/](https://www.geeksforgeeks.org/php-gmagickpixel-getcolor-function/)

**GmagickPixel：：getcolor()函数**是 PHP 中的一个内置函数，用于获取 GmagickPixel 对象以字符串或数组形式描述的颜色。 如果颜色设置了不透明度通道，则该值将作为列表中的第四个值提供。

**语法：**

```
*mixed* GmagickPixel::getcolor( *bool* $as_array,
                  *bool* $normalized_array )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$as_array (optional):** it specifies whether to get the value as an array. Its default value is False.
*   **$NORMAIZED_ARRAY (optional):** specifies whether to get the canonical array. Its default value is False.

**返回值：**此函数返回一个字符串或颜色值数组。

**异常：**此函数在出错时引发 GmagickPixelException。

下面给出的程序演示了 PHP 中的**GmagickPixel：：getcolor()函数**：

**程序 1(以字符串形式获取颜色)：**

```
<?php

// Create a new GmagickPixel object
// using __construct
$gmagickPixel = new GmagickPixel('#ccb062');

// Get the color
$color = $gmagickPixel->getcolor();
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(使用归一化获取颜色数组)：**

```
<?php

// Create a new GmagickPixel object
// using __construct
$gmagickPixel = new GmagickPixel('#ccb062');

// Get the color
$color = $gmagickPixel->getcolor(true, true);
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 3(在未归一化的情况下以数组形式获取颜色)：**

```
<?php

// Create a new GmagickPixel object
// using __construct
$gmagickPixel = new GmagickPixel('#ccb062');

// Get the color
$color = $gmagickPixel->getcolor(true, false);
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagickpixel.getcolor.php](https://www.php.net/manual/en/gmagickpixel.getcolor.php)
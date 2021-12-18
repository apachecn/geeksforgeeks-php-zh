# PHP|Imagick queryFontMetrics()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-queryfontmetrics-function/](https://www.geeksforgeeks.org/php-imagick-queryfontmetrics-function/)

Imagick：：queryFontMetrics()函数是 PHP 中的一个内置函数，用于返回表示字体度量的数组。 它将字体和文本作为参数，并返回表示字体度量的多维数组。

**语法：**

```php
*array* Imagick::queryFontMetrics( $properties, $text, $multiline )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$properties:** this parameter saves font properties.
*   **$TEXT:** this parameter saves text content.
*   **$multiline:** it holds multiple lines of parameters. If you leave it blank, it is automatically detected.

**返回值：**返回表示字体度量的多维数组。

下面的程序演示了 PHP 中的 Imagick：：queryFontMetrics()函数：

**Program：**此示例返回文本内容“GeeksForGeek”的字体属性。

```php
<?php
/* Create a new Imagick object */
$im = new Imagick();

/* Create an ImagickDraw object */
$draw = new ImagickDraw();

/* Set the font */
$draw->setFillColor( new ImagickPixel('grey') );

// Top left will be point of reference
$draw->setGravity( Imagick::GRAVITY_NORTHWEST );

/* Dump the font metrics, autodetect multiline */
var_dump($im->queryFontMetrics($draw, "GeeksForGeeks"));

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.queryfontmetrics.php](https://www.php.net/manual/en/imagick.queryfontmetrics.php)
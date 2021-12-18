# PHP|ImagickDraw setFillRule()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfillrule-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfillrule-function/)

**ImagickDraw：：setFillRule()函数**是 PHP 中的一个内置函数，用于设置绘制多边形时使用的填充规则。

**语法：**

```php
*bool* ImagickDraw::setFillRule( *int* $fill_rule )
```

**参数：**此函数接受单个参数**$FILL_RULE**，该参数保存与[FILLRULE 常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.fillrule-undefined)之一相对应的整数值。

下面给出了 FILLRULE 常量列表：

*   Imagick：：FILLRULE_UNDEFINED(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：setFillRule()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the Fill Rule
$draw->setFillRule(0);

// Get the Fill Rule
$fillRule = $draw->getFillRule();
echo $fillRule;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0 // Which corresponds to imagick::FILLRULE_UNDEFINED.
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the Fill Color
$draw->setFillColor('white');

// Set the Fill Rule
$draw->setFillRule(Imagick::FILLRULE_EVENODD);

// Translate the drawing
$draw->translate(40, 50);

// Start the path and draw pathlines
$draw->pathStart();

for ($x = 0; $x < 22; $x++) {
    if ($x >= 11) {
        $angle = fmod($x * 130, 360) * pi() / 180;
    } else {
        $angle = fmod($x * 98, 360) * pi() / 180;
    }
    $draw->pathLineToAbsolute(150 * sin($angle), 150 * cos($angle));
}

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/a9851e083115a3f255b030e39140dd6a.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setfillrule.php](https://www.php.net/manual/en/imagickdraw.setfillrule.php)
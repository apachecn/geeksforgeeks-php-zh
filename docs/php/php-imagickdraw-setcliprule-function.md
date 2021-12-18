# PHP|ImagickDraw setClipRule()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setcliprule-function/](https://www.geeksforgeeks.org/php-imagickdraw-setcliprule-function/)

**ImagickDraw：：setClipRule()函数**是 PHP 中的一个内置函数，用于设置裁剪路径要使用的多边形填充规则。 这通常不会对最终图像产生任何影响，但仍会提供不同的 FILLRULE 方法来完成相同的任务。

**语法：**

```
*bool* ImagickDraw::setClipRule( *int* $fill_rule )
```

**参数：**此函数接受单个参数**$FILL_RULE**，该参数保存一个与 FILLRULE 常量之一相对应的整数。

下面给出了 FILLRULE 常量列表：

*   Imagick：：FILLRULE_UNDEFINED(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：setClipRule()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the clipRule
$draw->setClipRule(imagick::FILLRULE_NONZERO);

// Get clipRule
echo $draw->getClipRule();
?>
```

发帖主题：Re：Колибри0.7.0

```
2 // which corresponds to imagick::FILLRULE_NONZERO.
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(500, 250, 'green');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$draw->setClipRule(imagick::FILLRULE_EVENODD);

$draw->setFontSize(24);

$draw->annotation(160, 125, 
                  'The clipRule is '
                  . $draw->getClipRule() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8d272f9223751e624a754aa89e2f60d5.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setcliprule.php](https://www.php.net/manual/en/imagickdraw.setcliprule.php)
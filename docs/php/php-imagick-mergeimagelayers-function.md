# PHP|Imagick mergeImageLayers()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-mergeimagelayers-function/](https://www.geeksforgeeks.org/php-imagick-mergeimagelayers-function/)

**Imagick：：mergeImageLayers()函数**是 PHP 中的内置函数，用于将图像层合并为一个。

**语法：**

```
*Imagick* Imagick::mergeImageLayers( *int* $layer_method )
```

**参数：**此函数接受单个参数**$layer_method**，该参数保存与[LAYERMETHOD 常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.layermethod-undefined)之一相对应的整数值。 您也可以像*mergeImageLayers(Imagick：：LAYERMETHOD_COMPAREANY)*那样直接传递常量。

LAYERMETHOD 常量列表如下：

*   Imagick：：LAYERMETHOD_UNDEFINED(0)
*   Imagick：：LAYERMETHOD_COALESS(1)
*   Imagick：：LAYERMETHOD_COMPARAREANY(2)
*   Imagick：：LAYERMETHOD_COMPARARECLEAR(3)
*   Imagick：：LAYERMETHOD_COMPARAREOVERLAY(4)
*   Imagick：：LAYERMETHOD_Dispose(5)
*   Imagick：：LAYERMETHOD_OPTIMIZE(6)
*   Imagick：：LAYERMETHOD_OPTIMIZEPLUS(7)
*   Imagick：：LAYERMETHOD_OPTIMIZEIMAGE(8)
*   Imagick：：LAYERMETHOD_OPTIMIZETRANS(9)
*   Imagick：：LAYERMETHOD_REMOVEDUPS(10)
*   Imagick：：LAYERMETHOD_REMOVEZERO(11)
*   Imagick：：LAYERMETHOD_COMPORT(12)
*   Imagick：：LAYERMETHOD_MERGE(13)
*   Imagick：：LAYERMETHOD_FLATTEN(14)
*   Imagick：：LAYERMETHOD_MOSAIC(15)

**返回值：**此函数返回包含新图像的 Imagick 对象。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：mergeImageLayers()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Add another image in the same object
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191126190119/geeksforgeeks-copy.png'));

// Set the Opacity
$imagick->setImageOpacity(0.5);

// Merge the Layers
$result = $imagick->mergeImageLayers(Imagick::LAYERMETHOD_FLATTEN);

// Display the image
header("Content-Type: image/png");
echo $result->getImageBlob();
?>
```

**输出：**
![](img/7881adac3a7a987b1a6aeb4000c81497.png)

**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Add another image in the same object
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191126191401/geeksforgeekshalf.png'));

// Set the Opacity
$imagick->setImageOpacity(0.7);

// Merge the Layers
$result = $imagick->mergeImageLayers(11);

// Display the image
header("Content-Type: image/png");
echo $result->getImageBlob();
?>
```

**输出：**
![](img/94f3c0197ad10a304674982b1bf54f0c.png)

**引用：**[https://www.php.net/manual/en/imagick.mergeimagelayers.php](https://www.php.net/manual/en/imagick.mergeimagelayers.php)
# PHP|Imagick addImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-addimage-function/](https://www.geeksforgeeks.org/php-imagick-addimage-function/)

**Imagick：：addImage()函数**是 PHP 中的一个内置函数，用于将新图像添加到 Imagick 对象图像列表。 操作后，迭代器位置移到列表末尾。 此函数用于从源对象的当前位置向 Imagick 对象添加新图像。 Imagick 类能够同时保存和操作多个图像。

**语法：**

```
*bool* Imagick::addImage ( $source )
```

**参数：**此函数接受保存源 Imagick 对象的单个参数*$source*。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

以下程序说明 PHP：
**原始图像 1：**
![adpative thresold image](img/92655fac130f4772488bfafcfb48fc6d.png)中的**Imagick：：addImage()**函数

**原始图像 2：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序：**

```
<?php 

// require_once('path/to/vendor/autoload.php');

header('Content-type: image/png');

$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$t = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/adaptiveThresholdImage.png');

$image->addImage($t);

echo $image;
?>
```

**Output:**![adaptive thresold image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**相关文章：**

*   [PHP|Imagick addNoiseImage()函数](https://www.geeksforgeeks.org/php-imagickaddnoiseimage-function/)
*   [PHP|Imagick AdaptiveBlurImage()函数](https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/)

**引用：**[http://php.net/manual/en/imagick.addimage.php](http://php.net/manual/en/imagick.addimage.php)
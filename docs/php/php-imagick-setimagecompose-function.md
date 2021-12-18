# PHP|Imagick setImageCompose()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagecompose-function/](https://www.geeksforgeeks.org/php-imagick-setimagecompose-function/)

**Imagick：：setImageCompose()函数**是 PHP 中的一个内置函数，用于设置与图像相关联的复合运算符。 此函数用于指定使用*Imagick：：MontageImage()*方法时如何合成图像缩略图。

**语法：**

```
*bool* Imagick::setImageCompose( *int* $compose )
```

**参数：**此函数接受包含图像合成运算符的单个参数**$compose**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageCompose()函数**：

**程序 1：**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compose
$imagick->setImageCompose(70);

// Get the Compose
$compose = $imagick->getImageCompose();
echo $compose;
?>
```

发帖主题：Re：Колибри0.7.0

```
70
```

**程序 2：**

```
<?php

// Create new Imagick Object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add label for first image
$imagick->labelImage('Image 1');

// Set the Compose for first image
$imagick->setImageCompose(10);

$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'));

// Add label for second image
$imagick->labelImage('Image 2');
// Set the Compose for second image
$imagick->setImageCompose(30);

// Create a Montage of Images
$draw = new ImagickDraw();
$draw->setStrokeColor('black');
$draw->setFillColor('white');
$draw->setStrokeWidth(1);
$draw->setFontSize(24);

$montage = $imagick->montageImage($draw, "3x2+0+0", "200x160+3+3>",
                 Imagick::MONTAGEMODE_CONCATENATE, "10x10+2+2");

// Display the output
$montage->setImageFormat('png');
header("Content-Type: image/png");
echo $montage->getImageBlob();
?>
```

**输出：**
![](img/88ef841361770796721734e897aa8c22.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagecompose.php](https://www.php.net/manual/en/imagick.setimagecompose.php)
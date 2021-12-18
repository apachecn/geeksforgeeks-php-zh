# PHP|Imagick recortImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-distortimage-function/](https://www.geeksforgeeks.org/php-imagick-distortimage-function/)

**Imagick：：recortImage()**函数是 PHP 中的一个内置函数，用于使用各种失真方法对图像进行失真。

**语法：**

```
*bool* Imagick::distortImage( $method, $arguments, $bestfit )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$method：**此参数存储图像失真方法的值。
*   **$Arguments：**此参数将扭曲方法的变量值存储为数组。
*   **$method：**此参数存储尝试调整目标大小以适应扭曲的源的方法类型的值

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/f3f9ad737830ec5f484ea0965e65694b.png)

下面的程序演示了 PHP 中的**Imagick：：TrusitImage()**函数：

**程序：**

```
<?php 

/*Imagick Object*/
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png');

$points = array(
    0, 0,
    55, 25,
    100, 0,
    100, 50
);

$imagick->setimagebackgroundcolor("lightgreen");
$imagick->setImageVirtualPixelMethod(\Imagick::VIRTUALPIXELMETHOD_BACKGROUND);

/* distortImage */
$imagick->distortImage(\Imagick::DISTORTION_AFFINE, $points, true);

/*Image Header*/
header("Content-Type: image/jpeg");
echo $imagick;
?>
```

**输出：**
![](img/51306a1b4f735dff43455178cea7c715.png)

**引用：**[http://php.net/manual/en/imagick.distortimage.php](//php.net/manual/en/imagick.distortimage.php)
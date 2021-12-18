# PHP|Imagick swirlImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-swirlimage-function/](https://www.geeksforgeeks.org/php-imagick-swirlimage-function/)

**Imagick：：swirlImage()**函数是 PHP 中的一个内置函数，用于围绕图像中心旋转像素。 阶数表示移动每个像素的弧线扫描程度。

**语法：**

```
*bool* Imagick::swirlImage( *float* $degrees )
```

**参数：**此函数接受单个参数*$度*，该参数定义旋转效果的紧密程度。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：swirlImage()**函数：

**程序：**

```
<?php 

// Create a Imagick object 
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Swirl the image
$imagick->swirlImage(350); 

header('Content-type: image/png'); 

// Display the output image 
echo $imagick; 

?> 
```

**输出：**
![](img/b6e50e798860349936fc1d8c0c6320dd.png)

**引用：**[https://www.php.net/manual/en/imagick.swirlimage.php](https://www.php.net/manual/en/imagick.swirlimage.php)
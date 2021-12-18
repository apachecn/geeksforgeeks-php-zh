# PHP|GmagickDraw setfiulity()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfillopacity-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfillopacity-function/)

GmagickDraw：：setfiopacity()函数是 PHP 中的一个内置函数，用于设置绘图图像的不透明度。 它在使用填充颜色或填充纹理绘制图像时使用。

**语法：**

```php
*public* GmagickDraw::setfillopacity( $fill_opacity ) : GmagickDraw
```

**参数：**此函数接受单个参数*$Fill_opacity*，该参数用于将不透明度的值保存为浮点型。

**返回值：**此函数在成功时返回 GmagickDraw 对象。

下面的程序演示了 PHP 中的 GmagickDraw：：setfiopacity()函数：

**程序 1：**

```php
<?php

// require_once('vendor/autoload.php');

// Create GmagickDraw object
$draw = new \GmagickDraw ();

// Set the strike color
$draw->setStrokeColor('Green');

// Use setFillColor() Function
$draw->setFillColor('Red');

// Use setFillOpacity() Function 
$draw->setFillOpacity(0.2);

$draw->setStrokeWidth(7);

// Create rectangle
$draw->rectangle(40, 30, 200, 260);

// Use setFillColor() Function
$draw->setFillColor('Red');

// Create rectangle of given size
$draw->rectangle(260, 30, 400, 260);

// Create an Gmagick object
$image = new \Gmagick ();

$image->newImage(500, 300, 'white');

// Set the image format
$image->setImageFormat("png");

// Render the draw commands in the 
// GmagickDraw object into the image.
$image->drawImage($draw);

// Send the image to the browser
header("Content-Type: image/png");
echo $image->getImageBlob();

?>
```

**输出：**
![setFillOpacity](img/3dfd1da6546bc95fb3674121a6b2aa7a.png)

**程序 2：**

```php
<?php

// require_once('path/vendor/autoload.php');

// Create new GmagickDraw object
$draw = new \GmagickDraw ();

// Set the stroke color
$strokeColor = new \GmagickPixel('Green');

// Set the filled color
$fillColor = new \GmagickPixel('Red');

// Set the stroke color
$draw->setStrokeColor('Green');

// Set the filled color
$draw->setFillColor('Red');

// Use setFillOpacity() Function
$draw->setFillOpacity(0.5);

// Set the stroke width
$draw->setStrokeWidth(2);

$smoothPointsSet = [ [
          ['x' => 10.0 * 5, 'y' => 10.0 * 5],
          ['x' => 30.0 * 5, 'y' => 90.0 * 5],
          ['x' => 25.0 * 5, 'y' => 10.0 * 5],
          ['x' => 50.0 * 5, 'y' => 50.0 * 5], ] ];

foreach ($smoothPointsSet as $points) {
    $draw->bezier($points);
}

// Create an image object
$gmagick = new \Gmagick ();

$gmagick->newImage(300, 300, 'White');

// Set the image format
$gmagick->setImageFormat("png");

// Render the draw commands in the
// GmagickDraw object into the image.
$gmagick->drawImage($draw);

// Send the image to the browser
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![setFillOpacity](img/61b61957215e2b547bd73f7b51442d00.png)

**引用：**[http://php.net/manual/en/gmagickdraw.setfillopacity.php](http://php.net/manual/en/gmagickdraw.setfillopacity.php)
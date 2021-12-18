# PHP|ImagickDraw 仿射()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-affine-function/](https://www.geeksforgeeks.org/php-imagickdraw-affine-function/)

**ImagickDraw：：affine()函数**是 PHP 中的一个内置函数，用于调整当前仿射变换矩阵。

**语法：**

```
*bool* ImagickDraw::affine( *array* $affine )
```

**参数：**此函数接受单个参数**$affine**，该参数保存包含仿射矩阵参数的数组。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：affine()函数**：

**程序 1：**

```
<?php
// Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object with 
// green background
$imagick->newImage(800, 250, 'green');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Translate the object
$draw->translate(100, 100);

// Apply the affine() function
$draw->affine(array("sx" => 7, "sy" => 1,
                    "rx" => 9, "ry" => 0,
                    "tx" => 200, "ty" => 0));

// Draw a rectangle
$draw->rectangle(-50, -50, 50, 50);

// Render the draw commands in the ImagickDraw object
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/4ce03ce490372e1981becb3c078e4aef.png)

**程序 2：**

```
<?php
//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object with 
// purple background
$imagick->newImage(800, 250, 'purple');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Translate the object
$draw->translate(100, 100);

// Apply the affine() function
$draw->affine(array("sx" => 2, "sy" => 1, 
                    "rx" => 0, "ry" => 0, 
                    "tx" => 0, "ty" => 0));

// Draw a rectangle
$draw->rectangle(0, -50, 50, 50);

// Draw a rectangle
$draw->rectangle(100, 50, 150, 100);

// Draw a rectangle
$draw->rectangle(200, -10, 250, 90);

//  Render the draw commands in the ImagickDraw object
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/f9cfac211b6b4cd951735456e725b8e3.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.affine.php](https://www.php.net/manual/en/imagickdraw.affine.php)
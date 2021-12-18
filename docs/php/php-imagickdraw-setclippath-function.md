# PHP|ImagickDraw setClipPath()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setclippath-function/](https://www.geeksforgeeks.org/php-imagickdraw-setclippath-function/)

**ImagickDraw：：setClipPath()函数**是 PHP 中的一个内置函数，用于将命名剪切路径与图像相关联。 只要剪裁路径保持有效，则只会修改剪裁路径绘制的区域。

**语法：**

```
*bool* ImagickDraw::setClipPath( *string* $clip_mask )
```

**参数：**此函数接受保存剪辑蒙版的单个参数**$Clip_MASK**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：setClipPath()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the clipPath
$draw->setClipPath('nameOfClipPath');

// Get clip path
echo $draw->getClipPath();
?>
```

发帖主题：Re：Колибри0.7.0

```
nameOfClipPath
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'green');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Setup a clipPath
$draw->pushClipPath('myClipPath');
$draw->rectangle(100, 40, 200, 200);
$draw->popClipPath();
$draw->setClipPath('myClipPath');

// Extra commands which are going to 
// be ignore as they are outside the
// area of the clipPath
$draw->rectangle(10, 100, 400, 400);
$draw->line(100, 100, 400, 400);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/6711958d6e33677592134c81d4432845.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setclippath.php](https://www.php.net/manual/en/imagickdraw.setclippath.php)
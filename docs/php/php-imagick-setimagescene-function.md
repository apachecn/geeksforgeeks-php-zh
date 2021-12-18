# PHP|Imagick setImageScene()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagescene-function/](https://www.geeksforgeeks.org/php-imagick-setimagescene-function/)

**Imagick：：setImageScene()函数**是 PHP 中的内置函数，用于设置图像场景。 Scene 的值包含整数值。

**语法：**

```
*bool* Imagick::setImageScene( *int* $scene )
```

**参数：**此函数接受保存场景的单个参数**$scene**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageScene()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the scene
$imagick->setImageScene(500);

// Get the scene
$scene = $imagick->getImageScene();

echo $scene;
?>
```

发帖主题：Re：Колибри0.7.0

```
500
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the image scene
$imagick->setImageScene(6);

// Set the image colorspace
$imagick->setImageColorspace($imagick->getImageScene());

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/ca819f215159b8b9fe1c250a3dc2a0a1.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagescene.php](https://www.php.net/manual/en/imagick.setimagescene.php)
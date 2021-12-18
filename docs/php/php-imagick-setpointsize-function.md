# PHP|Imagick setPointSize()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setpointsize-function/](https://www.geeksforgeeks.org/php-imagick-setpointsize-function/)

**Imagick：：setPointSize()函数**是 PHP 中的内置函数，用于设置 Imagick 对象的磅大小。

**语法：**

```
*bool* Imagick::setPointSize( *int* $point_size )
```

**参数：**此函数接受单个参数**$point_size**，该参数保存点的大小。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setPointSize()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set point size
$imagick->setPointSize(50);

// Create a caption
$imagick->newPseudoImage(800, 250, "caption:GeeksforGeeks");

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/37866893610854af23c0c172bf84d84d.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set point size
$imagick->setPointSize(400);

// Create a caption
$imagick->newPseudoImage(800, 250, "caption:GeeksforGeeks");

// Add border
$imagick->borderImage('black', 1, 1);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/94c827f6986c427b60de2b19e8414f7f.png)

**引用：**[https://www.php.net/manual/en/imagick.setpointsize.php](https://www.php.net/manual/en/imagick.setpointsize.php)
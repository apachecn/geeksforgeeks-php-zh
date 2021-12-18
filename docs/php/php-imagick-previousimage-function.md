# PHP|Imagick previousImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-previousimage-function/](https://www.geeksforgeeks.org/php-imagick-previousimage-function/)

**Imagick：：PreviousImage()函数**是 PHP 中的一个内置函数，用于移动到 Imagick 实例中的上一个图像。 Imagick 实例可以由其中的图像列表组成，Imagick previousImage()将指针/光标移动到 Imagick 实例中图像列表中的上一个图像。

**语法：**

```
*bool* Imagick::previousImage( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的 Imagick：：PreviousImage()函数：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Add a image to the imagick object.
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png'));

// Get the index
$index1 = $imagick->getIteratorIndex();
echo 'Before: ' . $index1 . '<br>';

// Move the cursor to first image
$imagick->previousImage();
$imagick->previousImage();

// Get the index
$index2 = $imagick->getIteratorIndex();
echo 'After: ' . $index2 . '<br>';
?>
```

发帖主题：Re：Колибри0.7.0

```
Before: 1
After: 0
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Add a image to the imagick object.
$imagick->addImage(new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'));

// Move the cursor to first image
$imagick->previousImage();
$imagick->previousImage();

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d2cdeddf65779f170b39764ad552411f.png)

**引用：**[https://www.php.net/manual/en/imagick.previousimage.php](https://www.php.net/manual/en/imagick.previousimage.php)
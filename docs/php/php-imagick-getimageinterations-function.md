# PHP|Imagick getImageInterations()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageinterations-function/](https://www.geeksforgeeks.org/php-imagick-getimageinterations-function/)

**Imagick：：getImageIterations()函数**是 PHP 中的一个内置函数，用于获取图像迭代。 迭代意味着帧自身应该重复多少次。

**语法：**

```
*int* Imagick::getImageIterations( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像或帧迭代的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：getImageIterations()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the interations
$iterations = $imagick->getImageIterations();
echo $iterations;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191120143630/newanimated.gif');

// Get the interations
$iterations = $imagickAnimation->getImageIterations();
echo $iterations;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimageiterations.php](https://www.php.net/manual/en/imagick.getimageiterations.php)
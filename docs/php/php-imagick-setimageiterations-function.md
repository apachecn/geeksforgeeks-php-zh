# PHP|Imagick setImageIterations()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageiterations-function/](https://www.geeksforgeeks.org/php-imagick-setimageiterations-function/)

**Imagick：：setImageIterations()函数**是 PHP 中的内置函数，用于设置图像迭代。 这里的迭代实际上是指帧自身应该重复多少次。

**语法：**

```php
*bool* Imagick::setImageIterations( *int* $iterations )
```

**参数：**此函数接受保存迭代次数的单个参数**$iterations**。 设置为 0 可使其永远循环。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageIterations()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191120143630/newanimated.gif');

foreach ($imagickAnimation as $frame) {

    // Add delay of 3 seconds
    $frame->setImageDelay(300);
}

// Set the interations
$imagickAnimation = $imagickAnimation->coalesceImages();
$imagickAnimation->setImageIterations(1);

// Display the image
header("Content-Type: image/gif");
echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/80402c96c1faf6b52026bbf2c9ddb4c7.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191120143630/newanimated.gif');

// Set the interations to 0 (infinite loop)
$imagickAnimation = $imagickAnimation->coalesceImages();
$imagickAnimation->setImageIterations(0);

// Display the image
header("Content-Type: image/gif");
echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/46dd7fcf2a4bc4fbc5c04d5e9793b1cd.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageiterations.php](https://www.php.net/manual/en/imagick.setimageiterations.php)
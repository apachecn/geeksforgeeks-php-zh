# PHP|Imagick sigmoidalContrastImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-sigmoidalcontrastimage-function/](https://www.geeksforgeeks.org/php-imagick-sigmoidalcontrastimage-function/)

**Imagick：：sigmoidalContrastImage()函数**是 PHP 中的一个内置函数，用于通过非线性 Sigmoid 对比度算法调整图像的对比度。

**语法：**

```php
*bool* Imagick::sigmoidalContrastImage( *bool* $sharpen, *float* $alpha,
                 *float* $beta, *int* $channel = Imagick::CHANNEL_DEFAULT)
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$Sharpen：**它指定是增大还是减小对比度。 True 值增加对比度，False 值降低对比度。
*   **$alpha：**它指定要应用的对比度。
*   **$beta：**它指定渐变的中点。
*   **$channel：**保持通道恒定的可选参数。 默认值为 Imagick：：Channel_Default。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：sigmoidalContrastImage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Adjust the contrast
$imagick->sigmoidalContrastImage(true, 10, 32000);

// Show the output
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/c691d7a99a88d591191266f365e4af0a.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Adjust the contrast
$imagick->sigmoidalContrastImage(false, 10, 31000);

// Show the output
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/d47d5799f87cd54920fcfa34202cabaa.png)

**引用：**[https://www.php.net/manual/en/imagick.sigmoidalcontrastimage.php](https://www.php.net/manual/en/imagick.sigmoidalcontrastimage.php)
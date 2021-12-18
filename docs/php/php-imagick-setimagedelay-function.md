# PHP|Imagick setImageDelay()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagedelay-function/](https://www.geeksforgeeks.org/php-imagick-setimagedelay-function/)

**Imagick：：setImageDelay()函数**是 PHP 中的内置函数，用于设置图像延迟。 对于动画图像，它是图像的帧在显示下一帧之前应该显示的时间量。 可以为图像中的每一帧单独设置延迟。

**语法：**

```
*bool* Imagick::setImageDelay( *Imagick* $delay )
```

**参数：**此函数接受单个参数**$delay**，该参数保存图像延迟的时间(以厘米为单位)。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageDelay()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

foreach ($imagickAnimation as $frame) {

    // Set the Delay to 3 seconds
    $frame->setImageDelay(300);
}

// Show the output
header("Content-Type: image/gif");

echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/c50115b9266c5406b8bb5b5799ea2fd7.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

foreach ($imagickAnimation as $frame) {

    // Set the Delay to 10 centiseconds
    $frame->setImageDelay(10);
}

// Show the output
header("Content-Type: image/gif");
echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/6d328ebf357b496869a89c7b81e916e4.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagedelay.php](https://www.php.net/manual/en/imagick.setimagedelay.php)
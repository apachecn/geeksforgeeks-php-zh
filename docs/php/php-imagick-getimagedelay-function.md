# PHP|Imagick getImageDelay()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagedelay-function/](https://www.geeksforgeeks.org/php-imagick-getimagedelay-function/)

**Imagick：：getImageDelay()函数**是 PHP 中的一个内置函数，用于获取图像延迟。 延迟实际上是在 gif 动画中从一个图像过渡到另一个图像所花费的时间。

**语法：**

```
*int* Imagick::getImageDelay( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，其中包含以厘米为单位的图像延迟(100centi=1 秒)。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：getImageDelay()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117145951/g4gnaimation1.gif');

foreach ($imagickAnimation as $frame) {
    $delay = $frame->getImageDelay();
    echo $delay . '<br>';
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191119143037/animatedcolor.gif');

foreach ($imagickAnimation as $frame) {
    $delay = $frame->getImageDelay();
    echo $delay . '<br>';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagedelay.php](https://www.php.net/manual/en/imagick.getimagedelay.php)
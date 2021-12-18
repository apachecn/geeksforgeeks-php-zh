# PHP|Imagick setSsamingFtors()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setsamplingfactors-function/](https://www.geeksforgeeks.org/php-imagick-setsamplingfactors-function/)

**Imagick：：setSsamingFtors()函数**是 PHP 中的一个内置函数，用于设置图像采样因子。

**语法：**

```php
*bool* Imagick::setSamplingFactors( *array* $factors )
```

**参数：**此函数接受单个参数**$factors**，该参数保存包含采样因子的关联数组。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setSsamingFtors()函数**：

**程序 1：**

## PHP

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Sampling factors
$imagick->setSamplingFactors(array('6', '7', '8'));

// Get the Sampling factors
$samplingFactors = $imagick->getSamplingFactors();
print("<pre>".print_r($samplingFactors, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => 6
    [1] => 7
    [2] => 8
)
```

**程序 2：**

## PHP

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the format to jpg
$imagick->setImageFormat('jpg');

// Set the sampling factors
$imagick->setSamplingFactors(array('1x1', '2x2'));

// Save the image
$compressed = $imagick->getImageBlob();

// Create a new imagick object
$reopen = new Imagick();

$reopen->readImageBlob($compressed);

// Resize it to same size
$reopen->resizeImage(667, 184, 0, 1);

// Show the output
header("Content-Type: image/jpg");
echo $reopen->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/50d1559f35462eed923275f005064f07.png)

**引用：**[https://www.php.net/manual/en/imagick.setsamplingfactors.php](https://www.php.net/manual/en/imagick.setsamplingfactors.php)
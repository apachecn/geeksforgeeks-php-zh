# PHP|Imagick 函数 Image()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-functionimage-function/](https://www.geeksforgeeks.org/php-imagick-functionimage-function/)

**Imagick：：FunctionImage()函数**是 PHP 中的内置函数，用于将算术、关系或逻辑表达式应用于伪图像。

**语法：**

```php
*bool* Imagick::functionImage( *int* $function, *array* $arguments,
                     *int* $channel = Imagick::CHANNEL_DEFAULT )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Function：**此参数保存要应用的函数。
*   **$Arguments：**此参数保存要传递给函数的数组。
*   **$channel：**此参数保存 Imagick 通道常量，这些常量提供对通道模式有效的任何通道常量。 可以使用按位运算符组合多个通道。 通道常量的默认值为 CHANNEL_DEFAULT。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：FunctionImage()函数**：

**程序 1：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create the pseudo image
$imagick->newPseudoImage(800, 200, 'gradient:green-white');

// Apply the functionImage() functions
$imagick->functionImage(Imagick::FUNCTION_SINUSOID, array(1, -90));

header("Content-Type: image/png");

// Display the output image
$imagick->setImageFormat("png");
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/36ec8bec3ada1ad6421bffb301c3bd3b.png)

**程序 2：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create the pseudo image
$imagick->newPseudoImage(800, 200, 'gradient:yellow-blue');

// Apply the functionImage() functions
$imagick->functionImage(Imagick::FUNCTION_POLYNOMIAL, array(6, -3, 1));

header("Content-Type: image/png");

// Display the output image
$imagick->setImageFormat("png");
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/01928ed97f608182c56c6da9f071de5d.png)

**程序 3：**

```php
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Create the pseudo image
$imagick->newPseudoImage(800, 200, 'gradient:white-blue');

// Apply the functionImage() functions
$imagick->functionImage(Imagick::FUNCTION_SINUSOID, array(3, -90));

header("Content-Type: image/png");

// Display the output image
$imagick->setImageFormat("png");
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/ad5251a0a9cf21b4e6e76e0f1cab7003.png)

**引用：**[https://www.php.net/manual/en/imagick.functionimage.php](https://www.php.net/manual/en/imagick.functionimage.php)
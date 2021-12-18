# PHP|ImagickPixel setHSL()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-sethsl-function/](https://www.geeksforgeeks.org/php-imagickpixel-sethsl-function/)

**ImagickPixel：：setHSL()函数**是 PHP 中的一个内置函数，用于使用色调、饱和度和亮度的规格化值设置 ImagickPixel 对象所描述的颜色。

**语法：**

```php
*bool* ImagickPixel::setHSL( *float* $hue, *float* $saturation, *float* $luminosity )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$hue：**它指定色调的规格化值。
*   **$饱和度：**它指定饱和度的规格化值。
*   **$发光度：**它指定发光度的规格化值。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixel：：setHSL()函数**：

**程序 1：**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the HSL for pixel
$imagickPixel->setHSL(0.4, 0.4, 0.4);

// Get the HSL of pixel
$HSL = $imagickPixel->getHSL();
print("<pre>".print_r($HSL, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [hue] => 0.40000158942082
    [saturation] => 0.4000152590219
    [luminosity] => 0.4
)
```

**程序 2：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator to iterate through each pixel
$imageIterator = $imagick->getPixelIterator();

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {
    // Loop through the pixels in the row
    foreach ($pixels as $column => $pixel) {

        // Get the current HSL
        $HSL = $pixel->getHSL();

        // Set the HSL and change only hue
        $pixel->setHSL(0.6, $HSL['saturation'], $HSL['luminosity']);

    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}

header("Content-Type: image/jpg");
echo $imagick;
?>
```

**输出：**
![](img/fe8290698279d269450974cbcde980fe.png)

**引用：**[https://www.php.net/manual/en/imagickpixel.sethsl.php](https://www.php.net/manual/en/imagickpixel.sethsl.php)
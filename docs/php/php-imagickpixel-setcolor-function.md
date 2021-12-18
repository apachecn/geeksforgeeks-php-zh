# PHP|ImagickPixel setColor()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-setcolor-function/](https://www.geeksforgeeks.org/php-imagickpixel-setcolor-function/)

**ImagickPixel：：setColor()函数**是 PHP 中的内置函数，用于设置 ImagickPixel 对象的颜色。

**语法：**

```php
*bool* ImagickPixel::setColor( *string* $color )
```

**参数：**此函数接受保存颜色的单个参数**$color**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickPixel：：setColor()函数**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the color
$imagickPixel->setColor('#428554');

// Get the color
$color = $imagickPixel->getColor();
print("<pre>".print_r($color, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [r] => 66
    [g] => 133
    [b] => 84
    [a] => 1
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
    if ($row % 5) {
        foreach ($pixels as $column => $pixel) {
            if ($column % 5) {
                // Set the color
                $pixel->setColor("green");
            }
        }
    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}

header("Content-Type: image/jpg");
echo $imagick;
?>
```

**输出：**
![](img/5d971dbf0b58a12c4f6f9851f0ffc704.png)

**引用：**[https://www.php.net/manual/en/imagickpixel.setcolor.php](https://www.php.net/manual/en/imagickpixel.setcolor.php)
# PHP|Imagick getImagesBlob()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagesblob-function/](https://www.geeksforgeeks.org/php-imagick-getimagesblob-function/)

**Imagick：：getImageBlob()函数**是 PHP 中的一个内置函数，用于将所有图像序列作为一个 BLOB 获取。 此函数对于动画 gif 非常有用，因为对它们执行*getImageBlob()*将不起作用。 此函数实现直接到内存的图像格式。

**语法：**

```php
*string* Imagick::getImagesBlob( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像的字符串。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getImagesBlob()**函数：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif');

// Show the output
header("Content-Type: image/gif");

echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/df7e9c5957f2cb509bf9afaa1f0bbbfd.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagickAnimation = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif');

foreach ($imagickAnimation as $frame) {

    // Apply blur to each frame
    $frame->blurImage(5, 3);
}

// Show the output
header("Content-Type: image/gif");

echo $imagickAnimation->getImagesBlob();
?>
```

**输出：**
![](img/478568935e5b5a8b82c40351aa5807b1.png)

**引用：**[https://www.php.net/manual/en/imagick.getimagesblob.php](https://www.php.net/manual/en/imagick.getimagesblob.php)
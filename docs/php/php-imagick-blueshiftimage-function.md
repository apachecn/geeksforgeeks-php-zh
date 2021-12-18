# PHP|Imagick BluShiftImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-blueshiftimage-function/](https://www.geeksforgeeks.org/php-imagick-blueshiftimage-function/)

**Imagick：：BlueShiftImage()**函数是 PHP 中的一个内置函数，用于将图像的颜色静音，以模拟月光下的夜间场景。

**语法：**

```php
*bool* Imagick::blueShiftImage( $factor)
```

**参数：**此函数接受单个参数*$factor*，该参数用于指定图像的静音颜色。

**返回值：**成功时此函数返回 True。

下面的程序**演示了 PHP 中的 Imagick：：BlueShiftImage()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using blueShiftImage function
$imagick->blueShiftImage(1.3);

header("Content-Type: image/jpg");
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/bb2c503c331b64f3fb21d38d6dc5811f.png)

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/cdn-uploads/gfg_200X200.png](img/980b01fe1c7f85a5a4bb0420eb28bb53.png)

```php
<?php

// Create new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/cdn-uploads/gfg_200X200.png');

// Using blueShiftImage function
$imagick->blueShiftImage(2.5);

header("Content-Type: image/jpg");
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/2e3f46c7e46088484ce08414579c5799.png)
**参考：**[http://php.net/manual/en/imagick.blueshiftimage.php](http://php.net/manual/en/imagick.blueshiftimage.php)